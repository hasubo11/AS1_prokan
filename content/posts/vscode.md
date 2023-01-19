---
title: "VisualStdioCode"
date: 
draft: True
---

# VSCodeの概要
VSCode(正式名称:**Visual Studio Code**)は，Microsoft社が提供するコードエディタである．

<img src="/VScode/1.png" alt="VSCodeのアイコン" width="200">

- [VScodeのインストール方法](#vscodeのインストール方法)
- [主な言語の使い方](#主な言語の使い方)
  - [C言語](#c言語)
  - [Python](#python)
- [その他便利な拡張機能](#その他便利な拡張機能)

# VScodeのインストール方法
1. VScodeをインストールするには[VScodeのサイト](https://azure.microsoft.com/ja-jp/products/visual-studio-code/)にアクセスし，「今すぐダウンロード」を選択

<img src="/VScode/2.png" alt="VSCodeのサイト" width="400">


2. インストールしたいデバイスのOSを選択

<img src="/VScode/3.png" alt="デバイス選択画面" width="400">

1. 選択すると```VSCode~~~.exe```という実行ファイルがダウンロードされるので実行

2. 実行したら，下のような画面が表示されるため，「同意する」を選択し「次へ」

<img src="/VScode/4.png" alt="exe実行時の最初の画面" width="400">

3. 下のような画面が表示されたら，全てのチェックを外し，「PATHへの追加」にチェック

<img src="/VScode/5.png" alt="オプション選択画面" width="400">

※ オプションの選択は任意だが，その他の2項目（エクスプローラーのディレクトリ~~~）にチェックを入れていくことで，下のように右クリックメニューにVSCodeが表示される

<img src="/VScode/6.png" alt="右クリック画面" width="400">

1. 「インストール」をクリック

<img src="/VScode/7.png" alt="インストール画面" width="400">

5. 「完了」をクリックし，一度PCを再起動すればインストール完了

<img src="/VScode/8.png" alt="最終画面" width="400">

# 主な言語の使い方
## C言語
- [GCCのインストール](#gccのインストール)
- [拡張機能のインストール](#拡張機能のインストールc言語)
- [実際に実行](#実際に実行c言語)

VSCodeでC言語及びC++を編集・実行可能にするためには，GCC(C言語のコンパイラ)と拡張機能をインストールする必要がある．

### GCCのインストール
1. [サイト](ttps://jmeubank.github.io/tdm-gcc/)からインストーラをダウンロード（Windowsの人はMinGW-w64を選択）
2. ダウンロードした```tdm64-gcc-~~~.exe```を実行
3. 実行後，以下の画面で「Create」を選択

<img src="/VScode/14.png" alt="" width="400">

4. 「MinGW-w64/TDM64」を選択し，「Next」

<img src="/VScode/15.png" alt="" width="400">

5. 保存先を参照(デフォルトでも可)し，「Next」

<img src="/VScode/16.png" alt="" width="400">

6. インストールする項目(デフォルトでも可)を選択し，「Install」

<img src="/VScode/17.png" alt="" width="400">

7. インストールが終われば「Next」->「Finish」で完了

### 拡張機能のインストール(C言語)

1. VSCodeの左端にある下の画像(Extensions)を選択

<img src="/VScode/10.png" alt="拡張機能アイコン" width="100">

2. 「Search Extensions~~~」に「C++」と入力し，下の画像の拡張機能を「install」

<img src="/VScode/9.png" alt="C++" width="400">

### 実際に実行(C言語)

1. 左端の一番上「Explorer」を選択し，「File->open Folder」でプログラムファイルを保存したフォルダを開く

<img src="/VScode/11.png" alt="フォルダの開き方" width="300">

2. フォルダを開いたら，右クリックし「New File...」を選択

<img src="/VScode/12.png" alt="ファイルの作り方" width="300">

3. ファイルの名前を```(プログラムファイルの名前).cpp```として保存すると下のようにC++のファイルが作成される

<img src="/VScode/13.png" alt="ファイルの作り方" width="400">

4. 例として，以下のコードを書き，保存する
```
//test.cppの中身
#include<stdio.h>

int main(void){
printf("Hello Would!");
}
```
5. 「Terminal -> New Terminal」でターミナルを開き，以下のコマンドを実行
```
gcc -o TEST test.cpp
```
コマンドを実行すると，下の画像のように```TEST.exe```という実行ファイルが作られる

<img src="/VScode/18.png" alt="方" width="400">

```TEST.exe```を実行し，以下のように表示されたら終了

<img src="/VScode/19.png" alt="方" wiSdth="300">

## Python
VSCodeでPythonを編集・実行可能にするためには，C言語同様に拡張機能をインストールする必要がある．

- [Pythonのインストール](#pythonのインストール)
- [拡張機能のインストール](#拡張機能のインストールpython)
- [実際に実行](#実際に実行python)
- [Pythonの便利なモジュール](#pythonの便利なモジュール)

### Pythonのインストール
1. [Pythonのサイト](https://pythonlinks.python.jp/)からインストーラをダウンロード (バージョンは任意だが，OSには気を付ける)

2. ダウンロードした```~.exe```を実行
3. 一番下の「Add Python 3.x to Path」にチェックし，「Install now」

<img src="/VScode/25.png" alt="" width="400">

### 拡張機能のインストール(Python)

1. VSCodeの左端にある下の画像(Extensions)を選択

<img src="/VScode/10.png" alt="拡張機能アイコン" width="100">

2. 「Search Extensions~~~」に「Python」と入力し，下の画像の拡張機能を「install」

<img src="/VScode/20.png" alt="Python" width="400">

### 実際に実行(Python)

1. 左端の一番上「Explorer」を選択し，「File->open Folder」でプログラムファイルを保存したフォルダを開く

<img src="/VScode/11.png" alt="フォルダの開き方" width="300">

2. フォルダを開いたら，右クリックし「New File...」を選択

<img src="/VScode/12.png" alt="ファイルの作り方" width="300">

3. ファイルの名前を```(プログラムファイルの名前).py```として保存すると下のようにC++のファイルが作成される

<img src="/VScode/21.png" alt="ファイルの作り方" width="400">

4. 例として，以下のコードを書き，保存する
```
##test.pyの中身
print("Hello Would!")
```
5. 「Ctrl + F5」で実行して以下のように表示されたら終了

<img src="/VScode/22.png" alt="" width="400">

### Pythonの便利なモジュール
Pythonには様々なモジュールが存在する．

* numpy
* matplotlib 
* pytorch

numpyやmatplotlibは，VSCode内からインストール可能である．
```
##numpyのインストール
pip3 install numpy

##matplotlibのインストール
pip3 install matplotlib
```
pytorchのインストールのみは他のモジュールとは異なる．
詳しくは[こちら](./torch.md)を参照してほしい．

# その他便利な拡張機能
VSCodeを使う上で便利な拡張機能を紹介する．
## 日本語化
以下の拡張機能をインストールすることで，日本語化可能

※インストールすると，右下にポップアップが表示されるので「Restart」を選択

<img src="/VScode/23.png" alt="" width="300">

## インデント管理
以下の拡張機能をインストールすることで，インデント管理が容易になる

<img src="/VScode/24.png" alt="" width="200">