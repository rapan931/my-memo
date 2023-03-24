# go

## 最新のgoをUbuntuにインストール

[参考](https://qiita.com/naotwu/items/2f8d63011b51499fbc46)

``` sh
cd /usr/local/
sudo wget https://dl.google.com/go/go1.19.4.linux-amd64.tar.gz
sudo tar zxf go1.19.4.linux-amd64.tar.gz 
sudo rm go1.19.4.linux-amd64.tar.gz 
go version
```

## gofmt で チェックが必要なファイル一覧の出力
- `gofmt -l .`

## go fmt でディレクトリ指定の全ファイルフォーマット
- `go fmt ./...`

## go mod

### 初期化

go mod init https://github.com/rapan931/xxxxxxx
