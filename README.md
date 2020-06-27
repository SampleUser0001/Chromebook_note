
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [Chomebook Note](#chomebook-note)
  - [概要](#概要)
  - [操作](#操作)
    - [ファイルマネージャを開く](#ファイルマネージャを開く)
    - [ファイルの扱い](#ファイルの扱い)
  - [実施したこと](#実施したこと)
    - [Linux（ベータ版）の有効化](#linuxベータ版の有効化)
    - [Textインストール](#textインストール)
    - [lifesizeインストール](#lifesizeインストール)
  - [パッケージ](#パッケージ)
    - [git](#git)
    - [docker](#docker)
      - [参考](#参考)
    - [docker-compose](#docker-compose)
    - [maven](#maven)
    - [python](#python)
    - [Atom](#atom)
  - [VSCode](#vscode)
    - [参考](#参考-1)
      - [インストール](#インストール)
    - [日本語化](#日本語化)
      - [フォントインストール](#フォントインストール)
      - [日本語入力機能](#日本語入力機能)
      - [日本語入力切り替え](#日本語入力切り替え)
        - [参考](#参考-2)
    - [Office](#office)
    - [Dropbox](#dropbox)
    - [Youtube](#youtube)
    - [Text](#text)
  - [端末そのものについて](#端末そのものについて)
    - [ディスク容量](#ディスク容量)
    - [ターミナルからアプリを起動する方法](#ターミナルからアプリを起動する方法)

<!-- /code_chunk_output -->

# Chomebook Note

## 概要

Chromium OS上で行ったことと課題のメモ

## 操作

### ファイルマネージャを開く

Alt + Shift + M

### ファイルの扱い

基本的にWeb上で管理される。（Google Drive）

## 実施したこと

### Linux（ベータ版）の有効化

1. 設定 → Linux（ベータ版）
2. メニュークリック

### Textインストール

https://chrome.google.com/webstore/detail/text/mmfbcljfglbokpmkimbfghdkjmjhdgbg?hl=ja

### lifesizeインストール

…できない！  
chromeでアクセスできるっぽい。  
マイクが有効かどうか確認したい。  
確認した。一応大丈夫そう。

## パッケージ

aptが使用できる。

```
sudo apt -y update
sudo apt -y upgrade
```

### git

最新ではないが、古くもないのでしばらく放置。

```
git version 2.20.1
```

### docker
インストールされていない。

```
sudo apt install docker
```

インストールするだけでは足りない。

```
cat /etc/group | grep docker
```

dockerグループがない場合実行。
```
sudo groupadd docker
```

```
sudo usermod -aG docker $USER
groups $USER
```

reboot.

#### 参考

https://www.virment.com/how-to-fix-couldnt-connect-to-docker-daemon/

### docker-compose

```
sudo apt install docker-compose
```

### maven

インストールされていない

```
sudo apt install maven
``` 

### python 

古い。
```
Python 2.7.16
```

3は別で入っている。
```
ittimfn@penguin:~$ python3 --version
Python 3.7.3
```

### Atom
後でもう一回入れたい。

## VSCode

当然入っていない。

```
curl -L "https://go.microsoft.com/fwlink/?LinkID=760868" > vscode.deb
sudo apt install ./vscode.deb
```

やはり日本語が表示できない。

### 参考
#### インストール
https://medium.com/satsangah/chromebook%E3%81%A7%E3%82%82visual-studio-code-%E3%82%92%E4%BD%BF%E3%81%8A%E3%81%86-f669a6e4d3b7

### 日本語化
フォントインストールと日本語入力機能が必要。

#### フォントインストール
```
sudo apt-get install fonts-noto
```

#### 日本語入力機能

```
sudo apt install -y fcitx-mozc
```

fcitxアプリを起動

```
fcitx-configtool
```

#### 日本語入力切り替え

ctrl + space

##### 参考
https://uepon.hatenadiary.com/entry/2019/02/03/192956

### Office

Dropbox上のExcelを開こうとしてみた。  
下記の２つの選択肢があるらしい。

- Excel for the web
- Google Sheets

Excel for the webは起動できた。  
GOogle Sheetsは起動できない。

### Dropbox

Webは行けるが…  
ローカルにマウントしたい。

### Youtube

再生できない。

ハードウェアアクセラレータをOffにすれば映るようだが、設定から見つからない。

### Text

エディタの一つ。

## 端末そのものについて

### ディスク容量

64GBモデルで40GBくらいの空き。

https://qiita.com/shibukawa/items/7200bd9d0afa6c0d4ed1

### ターミナルからアプリを起動する方法

調べる。