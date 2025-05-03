# gtiの使い方(ver.mac)
## 1.リポジトリの作成
### 1.1 ローカル(PC)側でリポジトリとなるフォルダを作成
```bash
mkdir <ディレクトリ名>
cd <ディレクトリ名>
```
### 1.2 1.1のフォルダをgitの使える環境にする
```bash
git init
git branch -M main
```
### 1.3 オンラインサーバとローカルのリポジトリを同期する
```bash
git remote add origin <URL>
```
## 2.リポジトリの変更の同期
### 2.1 ローカルでリポジトリを編集する
例
```bash
touch index.html
```
### 2.2 2.1の変更をオンラインサーバーに反映させる準備
```bash
git add .
git commit -m "コメント"
```
### 2.2 オンラインサーバーに反映させる
```bash
git push origin main
```
## 3.ブランチの作成
### 3.1 ブランチの作成と移動
ファイルの編集を行う前に以下のコマンドを実行する
```bash
git checkout -b <ブランチ名>
```
### 3.2 ブランチをオンラインサーバーに反映させる
ファイル編集後
```bash
git add .
git commit -m "コメント"
git push -u origin <ブランチ名>
```
### 3.3 ブランチとmainをマージしてオンラインサーバと同期させる
```bash
git checkout main
git merge <ブランチ名>
git push origin main 
```

##補足
### 1.リポジトリを最新状態にする方法
何かしらの理由でローカルのバージョンがオンラインサーバーより古い場合に使う
```bash
git pull origin main 
```
### 2.ブランチの確認
```bash
git branch
```
## 参考サイト
https://prog-8.com/docs/git-env
https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa
