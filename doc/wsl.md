# wsl

## コマンド

- ログイン後のフォルダ指定、distribution指定、ユーザ指定
  `wsl ~ -d NeoUbuntu -u rapan931`

- distribution一覧
  `wsl -l`

- distributionの退避
  `wsl --export #{WSL環境名} #{出力先ファイル名}`

- distributionのインポート
  NeoUbuntuという名前のdistributionをxxx.tarから、hogehogeディレクトリにインポート
  `wsl --import NeoUbuntu hogehoge xxx.tar`

## その他

- `Error: 0x80040326` が出たら
  - wsl --update
  - wsl --shutdown
  - [参考](https://akiki0106.hatenablog.com/entry/2023/03/30/114624)
