[TOC]

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

### maven

インストールされていない

### python 

古い。
```
Python 2.7.16
```

### Atom
日本語が表示できない。  
いい方法が見つからない。諦める。  

## VSCode

当然入っていない。

```
curl -L "https://go.microsoft.com/fwlink/?LinkID=760868" > vscode.deb
sudo apt install ./vscode.deb
```

やはり日本語が表示できない。

```
sudo apt-get install fonts-noto
```

### 参考
#### インストール
https://medium.com/satsangah/chromebook%E3%81%A7%E3%82%82visual-studio-code-%E3%82%92%E4%BD%BF%E3%81%8A%E3%81%86-f669a6e4d3b7

#### 日本語化
https://uepon.hatenadiary.com/entry/2019/02/03/192956

### Office

Dropbox上のExcelを開こうとしてみた。  
下記の２つの選択肢があるらしい。

- Excel for the web
- Google Sheets

### Dropbox

Webは行けるが…  
ローカルにマウントしたい。

### Youtube

再生できない。

ハードウェアアクセラレータをOffにすれば映るようだが、設定から見つからない。

### Text

エディタの一つ。

