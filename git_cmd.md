# git cmd

## git add について

- add で変更を記録したいファイルを指定することができる
  - git add .　で作業ディレクトリすべての変更を記録することになる

```sh
作業ツリーのすべての作業を記録する。(この段階ではまだまだ記録はされていない)
# git add .
```

## git commit について

- こいつでローカルリポジトリに対して変更の記録を行う。

```sh

変更内容を確認した上でコミットする
# git commit

コメント付きでコミットする
# git commit -m "コメント"

コミットする詳細情報を表示した上でコミットする
# git commit -v
```

## git status
- git add した情報と git commit した情報を確認することができる

```sh
こいつでgit のaddとcommitした情報を記録する。
# git status
```

```sh
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   git_cmd.md

no changes added to commit (use "git add" and/or "git commit -a")
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git add .
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   git_cmd.md

(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % 
```



