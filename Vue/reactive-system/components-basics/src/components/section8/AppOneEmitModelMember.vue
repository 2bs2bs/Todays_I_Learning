<template>
  <section>
    <h1>会員リスト</h1>
    <p>全会員の保有ポイントの合計: {{ totalPoints }}</p>
    <OneEmitModelMember
      v-for="[id, member] in memberList"
      v-bind:key="id"
      v-bind:id="id"
      v-bind:name="member.name"
      v-bind:email="member.email"
      v-model:points="member.points"
      v-bind:note="member.note"
    />
  </section>
</template>

<script setup lang="ts">
import { ref, computed } from "vue";
import OneEmitModelMember from "./OneEmitModelMember.vue";

// 会員リストデータの用意
const memberListInit = new Map<number, Member>();
memberListInit.set(33456, {id: 33456, name: "田中太郎", email: "bow@example.com", points: 35, note: "初回特典有り"});
memberListInit.set(47783, {id: 47783, name: "鈴木二郎", email: "mue@example.com", points: 53});

const memberList = ref(memberListInit);

// 会員リスト内の全会員のポイント合計の算出プロパティ
const totalPoints = computed(
(): number => {
  let total = 0;
  for(const member of memberList.value.values()){
    total += member.points;
  }
  return total;
}
);

// 会員情報インターフェース
interface Member {
id: number;
name: string;
email: string;
points: number;
note?: string;
}
</script>

<style scoped>
</style>