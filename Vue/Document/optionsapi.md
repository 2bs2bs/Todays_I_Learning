# Options Apiの基礎構文
```
export default defineComponent({
  name: "コンポーネント名",
  data(){
    return {
      データプロパティ名:
      ⋮
    }
  },
  computed: {
    算出プロパティ名(): データ型{
      算出処理
    },
    ⋮
  },
  methods: {
    メソッド名(): void {
      処理
    },
    ⋮
  }
});
```

算出プロパティやメソッド内でのデータプロパティへのアクセスには…
```
いいゾ～これコマンドキーがわからないWindowsと組み合わせたときのあれが不安じゃな〜よくわからんかもしれん…こっちのパチパチ感もかなりいいけどねあまりパチパチ言わない物言いぽいんどだけどthis.プロ
```