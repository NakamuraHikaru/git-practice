osawa
# How to git command
## リポジトリ作成
## 作業用ディレクトリ作成・移動
## 作業用ディレクトリの初期化
```
$ git init
```
## README.mdを作成
```
echo "# XXX" >> README.md
```
## 最初のコミットとプッシュ
`push`の際に、`-u`オプションを付けることで追跡ブランチを決める。
```
$ git add README.md
$ git commit -m "first commit"
$ git remote add origin https://github.com/XXXX/XXXXXX.git
$ git push -u origin master
```

## 作業した内容を確認してコミット
`diff`コマンドで差分を確認、`add`でステージに上げ、`status`でローカルの変更を確認。`diff --cached`で反映される変更を確認。  
最後に`commit`でコメントを付けてコミットする。
```
$ git diff XXXX
$ git add XXXX
$ git status
$ git diff --cached
$ git commit -m "XXXX"
```

## コミットした内容をプッシュする
追跡ブランチが定められていれば`git push`でよい、そうでなければ`-u`オプションで指定する。
```
$ git push (-u XXXX)
```

## ログを確認し、コミットの変更点を見る
`log`コマンドにより変更履歴を表示。
表示された変更履歴の中のハッシュ値をもとに`show`コマンドで変更点を確認する。
```
$ git log
$ git show XXXX
```

## ローカルブランチを確認
ローカルブランチが表示される。*がついているものが現在いるブランチ。
```
$ git branch
```

## ブランチの作成・切り替え
`branch`コマンドでブランチを作成することができる。`checkout`コマンドでブランチを移動することができる。
```
$ git branch XXXX
$ git checkout XXXX
```