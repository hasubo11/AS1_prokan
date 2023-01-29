---
title: "GitHub"
date: 2023-01-26
draft: true
---

# GitHubの概要
ソースプログラム等のバージョンを管理できるサービスである．
また，ソースコードの共有が容易であったり，履歴を残しながら編集・変更ができたりする．

# 事前知識
GitHubを使う上で必要な知識を解説する．
- リポジトリ
  - バージョン管理を行いたいファイルやディレクトリを，記録・管理する場所
  - ローカルリポジトリは自分のPC上のリポジトリ
  - リモートリポジトリは専用のサーバーなどに配置して複数人で共有するために利用するリポジトリ
- クローン
  - リモートリポジトリを自分のPC上にコピーする機能
- ブランチ
  - 変更履歴を分岐させて記録する機能
- コミット
  - ローカルリポジトリに変更を反映させること
- プッシュ
  - ローカルリポジトリの内容をリモートリポジトリに反映させること
- フォーク
  - 他のプログラマーのリポジトリをコピーして編集できる機能
- プルリクエスト
  - ローカルリポジトリでの変更を他のプログラマーに通知する機能
- マージ
  - プルリクエストを受け取ったレビューやマージ担当者が他の人の変更を自分のリポジトリに取り入れる機能

# GitHubの使用方法
1. Gitのインストール
Gitは，ローカルのパソコンで編集作業を行いファイルの修正履歴も管理できる分散型バージョン管理システムである．
そして，GitHubはGitを用いたソフトウェア開発プロジェクトのための共有ウェブサービスを指す．
つまり，「Gitはシステム，GitHubはGitを用いたサービス」ということである．
Windowsの場合は，[Git for Windows](https://gitforwindows.org/)からインストールしよう．
Macの場合は，[Download for macOS](https://git-scm.com/download/mac)からインストールしよう．
2. Gitの初期設定
インストールしたGitに対して自分のユーザー名とメールアドレスを登録しよう．
ここで登録した内容はリポジトリに対してコミットした人の情報として履歴などに表示される．
3. アカウント作成
[GitHubのサイト](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)にアクセスし，GitHubのアカウントを作成する．
必要な情報は，ユーザーネーム，メールアドレス，及びパスワードである．
4. リモートリポジトリを作成
   1. <img src="/GitHub/create_repo1.png" alt="create_repo" width="200">
    上記画像右上の「New」ボタンをクリック
    <img src="/GitHub/create_repo2.png" alt="create_repo" width="200">
    リポジトリネームを設定した後は，リポジトリの種類を決定する．
    「Public」はソースコードを公開する場合のことを指し，「Private」は公開したくない場合に選択する．
    READMEファイルを事前にリポジトリファイルの中に作成したい場合は，「Add a README file」にチェックする．
    最後に「Create repository」ボタンをクリックするとリポジトリの作成が完成する．
5. ローカルリポジトリの作成
下記のコマンドをWindowsなら「PowerShell」，Macなら「ターミナル」で入力することで，作業ディレクトリを作成する．
```
$ mkdir github
$ cd github
$ mkdir pushtest
$ cd pushtest
```
「git init」でローカルリポジトリを作成する．
```
$ git init
```
6. ファイルを作成
続いては，任意のテキストファイルをディレクトリ「test」に作成する．
```
$ vi test.txt
```
7. ローカルリポジトリにコミット
先ほどのtest.txtファイルをローカルリポジトリにコミットしてみよう．
```
$ git add test.txt
$ git commit -m 'コミットメッセージ'
```
8. リモートリポジトリにプッシュ
先ほどローカルリポジトリにコミットしたファイルをリモートリポジトリにプッシュする．
```
$ git remote add origin https://github.com/ユーザーID/test.git
$ git push origin master
```
ここで，ユーザーネームとパスワードを聞かれたらそれぞれGitHubで登録した内容を入力しよう．
これで完成です！！！！

# GitHubおまけ
1. GitHubでSSH接続したい
[GitHub SSH接続の方法](https://blog.cloud-acct.com/posts/u-github-ssh/)
2. VScodeでGitHubを使う方法
[VScodeでGitHubを使う方法](https://miya-system-works.com/blog/detail/vscode-github/)
3. SourceTreeでGitHubを使う方法
[SourceTreeでGitHubを使う](https://qiita.com/TAKANEKOMACHI/items/53058acc15d965d66798)