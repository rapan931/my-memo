# flutter

## windows

### install

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

### vscode

- flutter extensionを追加
  - wsl側のvscodeにインストールされないように、左下のアイコンからWSL接続切ってから実施する

- コマンドパレットから `run flutter doctor` 実行

### androidのemulator立ち上げ

- Android Studioを開く
- `More Action` から `Virtual Device Manager` を選択
- `Create Virtual Device` を選択
- 適当にDevice選択して Next
- System Imageをダウンロードして

### サンプルアプリ立ち上げ

- vscodeから `flutter new project`
- `Application` を選択し、適当なフォルダーを指定、その後project名を適当に決めてmain.dartを開いてF5で起動

### "[!] App requires Multidex support"というエラー

- でかいプラグイン等使って64000を超えるメソッドを使うとエラーになってしまう
- android\app\build.gradleの `minSdkVersion` を21(直値)に変更すると問題なくなる

## Linux

### install

- cd /usr/local
- sudo wget https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.7.8-stable.tar.xz
- sudo tar xf flutter_linux_3.7.8-stable.tar.xz 

- .bash_profileに `export PATH=$PATH:/usr/local/flutter/bin` 追記
- `flutter config --no-analytics`

### dartについて

- flutter/binには `dart` も含んでいるので、flutterをinstallしたのであればdartを削除する

- sudo apt purge dart 
```
❯❯ which dart
/usr/local/flutter/bin/dart
```

- 新しいdartになったので、 `dart --disable-analytics`


### Android SDK

- Linux toolchainのインストール `sudo apt install libgtk-3-dev`
- https://redirector.gvt1.com/edgedl/android/studio/install/2022.1.1.21/android-studio-2022.1.1.21-windows.exe
- cd /usr/local
- `sudo wget https://redirector.gvt1.com/edgedl/android/studio/ide-zips/2022.1.1.21/android-studio-2022.1.1.21-linux.tar.gz`
- tar ....
- cd android-studio/bin
- ./studio.sh
  - SDK Managerからcmdline-toolsをインストール
- flutter doctor --android-licenses

- Cheomeが見つからないとエラーが。。[これ](https://github.com/flutter/flutter/issues/65932)
  - WSLにLinuxのchromeをインストールする
  - cd /usr/local
  - wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
  - sudo apt install ./google-chrome-stable_current_amd64.deb

- flutter doctorで All OK!!!!

## Tips

- 不要なbuildは削除できる
```
$ flutter config --no-enable-android
$ flutter config --no-enable-ios
$ flutter config --no-enable-macos-desktop
$ flutter config --no-enable-windows-desktop
```

- プロジェクト名(?)と同じ名前のpackageはimportできない
  (providerプロジェクトでproviderパッケージを入れようとしたらflutter pub getでエラー)

