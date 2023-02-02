---
title: "TeX Liveのインストール方法"
date:
draft: true
---

# TeXの環境構築
## そもそもTeXとは？
TeXは著名なコンピュータ科学者 Donald E. Knuthによって生み出された最強の文書成型システムです．次のような特徴を持っています．

* 複雑な数式でもきれいに書ける．
* 論文の様な文書を作成するのに適している．
* Microsoft Windows， OS X， Unix互換OS(Linux OS， BSD系OS)，モバイルオペレーティングシステム(Android OS，iOSなど)等，多くのOS上で利用できる．
* TeXのソースファイルはテキストファイルなので，異なるシステムでもソースを共通に使え，電子メールでも簡単に交換できる．さらに，ソースファイルをTeXで処理して得られるDVIファイルもハードウェアに依存しない．
* フリーソフトウェアである．

この他にも図番号の自動割り振り等，便利な機能を備えたテキストエディタである．  
それでは早速，環境構築を始めましょう．

## TeXLive2022のインストール（Win版のみ）
以下の手順に従って**TeX Live**をインストールしてみましょう．

1. 以下のリンクにアクセスする．
* [**https://tug.org/texlive/**](https://tug.org/texlive/)

2. 自分のOSにあったインストーラーを選択する（今回は「**install on Windows**」）．
<img src="/TeX/installer_url.png" alt="" width="300">

3. インストーラーを起動すると以下の画面が出てくるので，詳細情報をクリックする．
<img src="/TeX/first_step.png/19.png" alt="" width="300">

4. 以下の画面で「**Install**」を選択して，画面の指示に従って「**Next >**」 をクリックして進んで行く．
<img src="/TeX/second_step.png/19.png" alt="" width="300">

5. 「**TeX Live インストーラー**」の画面が表示されるので，「**インストール**」をクリック
<img src="/TeX/third_step.png/19.png" alt="" width="300">

6. 以下の画面が表示されたらインストール完了です．
<img src="/TeX/fourth_step.png/19.png" alt="" width="300">

# TeXの基本的な書き方
TeXは基本的に「プリアンブル」 + 「ドキュメント」の2部構成担っています．
* プリアンブル：文書のスタイル（1段組みか2段組みか），上下左右の余白，タイトルのデザイン等，あらゆる書式を定義する箇所です．
* ドキュメント：```\begin{document}```と```\end{document}```に囲まれた箇所で，本文の内容を記述する箇所です．

簡単な文書フォーマとならばプリアンブルで設定できますが，学会や技術レポート等では通常専用の「スタイルファイル（拡張子は```.sty```）」が用意されており，それをプリアンブルで読み込むことで書式で決まります．同じスタイルファイルを使えば（途中で無理やり変えない限り）同じ書式で文書作成ができるので，著者は各学会の「書式的な決まり」を守りながら本文の記述だけに集中すれば問題ありません．．
プリアンブルで定義するテンプレートの例として以下のものを紹介します．

* [**http://hooktail.org/computer/index.php?TeX%A5%C6%A5%F3%A5%D7%A5%EC%A1%BC%A5%C8**](http://hooktail.org/computer/index.php?TeX%A5%C6%A5%F3%A5%D7%A5%EC%A1%BC%A5%C8)


# 環境構築めんどくさいなぁ...

<img src="/TeX/overleaf.png" alt="" width="300">

そんなあなたに，環境構築等面倒くさい設定をスキップして使用できるアイテムを紹介します．
## Overleaf
ブラウザ上で動作するTeXです．特に最近は複数のユーザで共同で編集できるので，複数人で行うプロジェクトであればこちらの方が便利かもしれませんね．

Overleafは[**コチラ**](https://www.overleaf.com/latex/templates)からアクセスできます．

デフォルトでは日本語で動作しないため以下のリンクをよく読んで設定をしてください
* [**https://doratex.hatenablog.jp/entry/20180503/1525338512**](https://doratex.hatenablog.jp/entry/20180503/1525338512)