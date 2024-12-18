# v-for

ループのディレクトリである`v-for`

## 基礎構文
```
v-for="各要素を格納する変数" in ループ対象
```
各要素を格納する変数はVueではエイリアスというらしい

インデックス値を利用するにはindexを使う
```
v-for=("エイリアス, indexを格納する変数") in ループ対象
```

! keyにindex値を入れたらだめ ！ → 状態がうまく保存できないため、間に挿入するとインデックス値がずれる

## 連想配列をループする`v-for`ディレクティブ
```
v-for="(各要素の値を格納する変数, 各要素のキーを格納する変数) in ループ対象"
```

## 連想配列でインデックス値を利用する場合のv-forディレクティブ
```
v-for="(各要素の値を格納する変数, 各要素のキーを格納する変数, インデックス値を格納する変数) in ループ対象"
```

## カウンタ変数を利用したループ
```
v-for="カウンタ変数 in 終端の値"
```