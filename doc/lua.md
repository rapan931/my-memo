# Lua

## lua-language-server

### build

```sh
$ cd ~/repos/github.com/sumneko/lua-language-server
$ git pull
$ git submodule update --depth 1 --init --recursive

$ cd 3rd/luamake
$ ./compile/install.sh
$ cd ../..
$ ./3rd/luamake/luamake rebuild

```

## re-build

```sh
git pull
git submodule update --depth 1 --init --recursive

cd 3rd/luamake
./compile/install.sh
cd ../..
./3rd/luamake/luamake rebuild
```

## Lualocks

### build

[see](https://github.com/luarocks/luarocks/wiki/Installation-instructions-for-Unix)
```sh
cd /usr/local/src
sudo wget https://luarocks.org/releases/luarocks-3.8.0.tar.gz
sudo tar zxpf luarocks-3.8.0.tar.gz
sudo cd luarocks-3.8.0

sudo ./configure --with-lua-include=/usr/local/include (failed......)

sudo apt install liblua5.1-dev
sudo ./configure --with-lua-include=/usr/include/lua5.1 (successed!!!!!)

sudo make
sudo make install
(finish!)
```

### install packages

(see)[https://github.com/notomo/vusted#installation]
```sh
luarocks --lua-version=5.1 install vusted
```

(depend)[https://github.com/notomo/vusted#installation]
```sh
sudo luarocks --lua-version=5.1 install copas
sudo apt install libev-dev
sudo luarocks --lua-version=5.1 install lua-ev scm --server=http://luarocks.org/repositories/rocks-scm/
sudo luarocks --lua-version=5.1 install moonscript
```

