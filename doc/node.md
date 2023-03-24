# node

## nvm

### install

- curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
- nvm install --lts
- 既にデフォルトがlatestだったので、以下は実行していない
  - nvm alias default lst/*

- npm i yarn -g

## node 

- npm init -y
- package.jsonを以下に変更
```
  "main": "index.js",
  "type": "module",
```

- npm i -D typescript @types/node
- npm i -D ts-node (ts-nodeも入れとく)
- npx tsc --init
- tsconfig.jsonを以下に変更
```
  "target": "es2020" // 値変更
  "module": "esnext" // 値変更
  "moduleResolution": "node" // コメントイン
  "outDir": "./dist" // コメントイン
  "compilerOptions": {
    // 個々にたくさんのオプションがあるけどここは変えない
  },
  "include": ["./src/**/*.ts"] // 追加
```

- src/index.ts作成
- npx tsc && node dist/index.js
  or 
  ts-node src/index.html


- npm install --save-dev eslint eslint-config-prettier prettier @typescript-eslint/parser @typescript-eslint/eslint-plugin
- npx eslint --init
- nvim .prettierrc
