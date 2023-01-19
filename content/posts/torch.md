---
title: "pytorch"
date: 
draft: True
---

# pytorchの概要
pytorchとは，Pythonで用いることができるモジュールである．

# pytorchのインストール
1. [pytorchのサイト](https://pytorch.org/get-started/locally/)からインストールコマンドを得る．(OSとompute Platfromは自身のPCに合わせて選択する)  
<img src="/VScode/26.png" alt="" width="400">  
```
## インストールコマンドの例
pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu117
```

2. 得られたインストールコマンドをVSCodeのターミナルで実行し，インストール

# 仮想環境
Pipenvを用いることで，仮想環境で実行可能になる

## Pipenvの初期設定
1. プロジェクトのディレクトリ内に```.venv```を作成したいので，環境変数を登録する  
```
export PIPENV_VENV_IN_PROJECT=1
export PIPENV_SKIP_LOCK=1
```
上のコマンドをターミナルで打ち込むか，```~/.bashrc```に直接書き込む．

2. 設定が終われば，以下のコマンドで仮想環境を作成  
```
pipenv --python 3.x  ##3.xでvenv環境を作成
```

## モジュールのインストール
仮想環境でのモジュールのインストールは```pip3```ではなく，```pipenv```を用いる  
```
## 例:numpyのインストール
pipenv install numpy
```

pytorchのインストールは2種類の方法が存在する．
### 仮想shellに入りインストール
Pipenv環境を作成後，```pip shell```でサブプロセスを起動し，コマンドを実行する．

### ショートカットを作成しインストール
Pipfile内の[script]ブロックにショートカットコマンドを登録出来るので，ここにpytorchインストールコマンドのショートカットを作成する．  
```
## Pipfileの内容の例
[[source]]
name = "pypi"
url = "https://pypi.org/simple"
verify_ssl = true

[dev-packages]

[packages]

[requires]
python_version = "3.8"

+ [scripts]
+ torch = "pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu117"
```

変更後，ターミナルで```pipenv run torch```と入力し，実行するとインストールが始まる．



# 関連記事
[VSCodeの概要](/posts/vscode/)