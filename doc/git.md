# git

## commit prefix

- feat      feature
- fix       bug fix
- docs      documentation
- style     formatting, missing semi colons, etc
- refactor  refactoring
- test      when adding missing tests
- chore     maintain

- deps      dependencies
- breaking  breaking changes

## gh

### create repository

- gh repo create <prj-name> --public --clone --license mit
- gh repo create <prj-name> --public --clone --license mit --add-readme
  -> --add-readmeが使えず。。バージョンが古いせいかも

### create pr

- gh pr create -w (今いるブランチでプルリク作成＆ブラウザ開く)

## ghq

- ghq list -p <repo-name>
- ghq list -p 
- ghq root
