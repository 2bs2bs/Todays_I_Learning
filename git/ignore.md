# どんなファイルを管理したくないか
- passwordなどの機密情報
- 必要ないファイル

# .gitignoreの書き方
```
# #はコメント

# 指定したファイルを除外
index.html

# rootディレクトリを指定
/root.html

# ディレクトリ以下を除外
dir/

# /以外の文字列にマッチ
/*/*.css
```
.gitignoreに記載された瞬間から追跡されなくなっているみたい
