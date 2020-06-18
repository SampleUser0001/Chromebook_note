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

### Office

Dropbox上のExcelを開こうとしてみた。  
下記の２つの選択肢があるらしい。

- Excel for the web
- Google Sheets

### Dropbox

Webは行けるが…  
ローカルにマウントしたい。

## 課題

- Youtubeが再生できない
    - ハードウェアアクセラレータをOffにすれば映るようだが、設定から見つからない。
- Linuxから日本語入力できるエディタがない
    - 一応Textがあるが、Linuxから起動できるエディタを探す。
- Slackにログインできない
    - ブラウザ版を使用する。
- 開発環境を整える（まだ確認していないもの込）
    - エディタ
        - viはある。
    - git
    - docker
    - maven
    - python
    - Office