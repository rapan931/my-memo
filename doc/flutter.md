# flutter

## install

- 公式からinstall
- path通す
- flutter doctor実行
- android studio install
- `flutter config --android-studio-dir="C:\Program Files\Android\AndroidStudio"` を実行
- android studioでflutterプラグインをinstall
- SDK Managerを起動して以下をインストール
  - Google USB Driver
  - Android SDK Command-line Tools
- `flutter doctor --android-licenses`
- Visual Studioインストール(VSCodeではない)
  - C++によるデスクトップ開発と、C++によるモバイル開発も一応追加。
- `flutter doctor`
  - Windows10以上かが確認できないと出るが、無視。
    https://github.com/flutter/flutter/issues/117890

## vscode

- flutter extensionを追加
  - wsl側のvscodeにインストールされないように、左下のアイコンからWSL接続切ってから実施する

- コマンドパレットから `run flutter doctor` 実行

## androidのemulator立ち上げ

- main.dartを開いてステータスバー下部の `windows` を1クリック


## サンプルアプリ立ち上げ

- vscodeから `flutter new project`
- `Application` を選択し、適当なフォルダーを指定、その後project名を適当に決めてmain.dartを開いてF5で起動


