# dart

## install

- sudo apt update
- sudo apt install apt-transport-https
- wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo gpg --dearmor -o /usr/share/keyrings/dart.gpg
- echo 'deb [signed-by=/usr/share/keyrings/dart.gpg arch=amd64] https://storage.googleapis.com/download.dartlang.org/linux/debian stable main' | sudo tee /etc/apt/sources.list.d/dart_stable.list

- sudp apt update
- sudo apt install dart

## setting

- 解析結果は送信しないようにする
  dart --disable-analytics

## 構文

- lambda式は１行なら=>を入れて、複数行なら=>が無し。
- 型につく `?` はNullableを提示する

```
int? v;
print(v.runtimeType);  // Null
print(v is int);       // false
print(v is int?);      // true

v = 10;                // この時点で non-nullable
print(v.runtimeType);  // int
print(v is int);       // true
print(v is int?);      // true
```

- async/await, streamについては[ここ](https://medium.com/@kawanojieee/dart-async-await-394846fb3d2c)参照

- await forとlistenの違いはstreamの終了を待つか。名前の通りawait forが待つ。
  [参考](https://qiita.com/shindex/items/1ec40cc224aedcf31946)
