# Hello, Pull Request

## Outline
This is a remote repository named "pullRequestPrac".

## Goal

**(簡単な)Pull Requestを使ったチーム開発を行えるようになること。**



## Outline

1. リモートリポジトリを手元のPC(ローカル)にコピー(クローン)する。
2. 機能拡張用ブランチを作成する。(これは、もとのコードを傷つけないようにするため。)
3. 機能拡張ができたら変更をリモートリポジトリに反映(push)させる。


以下の作業はGitHub上で行うため説明は省略する。

4. Pull Requestを作成する。



## Before you get started

GitHubアカウントを持っていない場合,[ここ](http://www.aise.ics.saitama-u.ac.jp/~gotoh/IntroOfGitOnMacOSX.html#toc35)を参考にしてアカウント登録を済ませること。




## Let's Start

### 1. リモートリポジトリを手元のPC(ローカル)にコピー(クローン)する。

- リモートリポジトリをクローンする

```
$ cd # ホームディレクトリに移動
$ git clone git@github.com:struuuuggle/pullRequestPrac_XX.git # XXには指定された数字を入れる
$ cd pullRequestPrac_XX # pullRequestPrac_XXに移動
```

### 2. 機能拡張用ブランチを作成する。

- 現在のブランチを確認

```
$ git branch                      # 現在どのブランチにいるか確認する
* master
```

- 機能拡張用ブランチを作成する。拡張機能に応じた命名がなされているとよい。

```
$ git checkout -b update-XXX   # 機能拡張用branchを作成。(update-XXXは拡張する機能に応じて名前を変更する。)
```

- 機能拡張する。
   各種エディタ等で作業を行う。

### 3. 機能拡張ができたら変更をリモートリポジトリに反映(push)させる。

```
$ git add -A                      # 変更のあったファイルを全て追加
$ git commit -m "Update XXX"      # 変更履歴をリポジトリに保存
$ push origin update-XXX          # リモートリポジトリにpushする
```

```
To git@github.com:struuuuggle/pullRequestPrac_XX.git

 * [new branch]      update-XXX -> update-XXX
```

push後に、上記ログが出ていることを確認。



## ひとこと

- よく使うコマンド

```
$ git status
$ git branch                             # 現在の変更状況を確認
$ git branch -b <branchname>             # branchを作成
$ git checkout <branchname>              # branchnameブランチに移動
$ git add <filename>                     # filenameファイルを追加
$ git add -A                             # 変更のあったファイルを全て追加
$ git commit (-a) -m "<commit message>"  # 変更履歴をリポジトリに保存
$ git push                               # ローカルリポジトリの内容をリモートリポジトリに反映させる
```

## Reference
[GitHub初心者はForkしない方のPull Requestから入門しよう | qnyp blog](http://blog.qnyp.com/2013/05/28/pull-request-for-github-beginners/)
