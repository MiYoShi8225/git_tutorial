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

## git diffについて
```sh
git addする前の変更分
# git diff
# git diff <ファイル名>


git addした後野変更分
# git diff --staged
```

## git log について

- gitのログ情報を確認するコマンド
```sh

# git log

情報を一行で表示する
# git log --oneline

ファイルの変更差分を表示する
# git log -p <ファイル名>

表示するコミット数を制限する
# git log -n <コミット数>
```


```sh
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git log
commit ad3daf6ed75d2efe71f86e4a28250539dd4b0f3c (HEAD -> master)
Author: MiYoShi8225 <down8225@gmail.com>
Date:   Sat Jun 26 23:24:27 2021 +0900

    git diffの情報を追加

commit 81cd31a5bbcd86974e3084203f8c8eaf1aeb71e6
Author: MiYoShi8225 <down8225@gmail.com>
Date:   Sat Jun 26 23:17:31 2021 +0900

    cmd 情報にstatusの情報を追加

commit 1c1391fb695ff5d2924b5c32b23834c735b09aec
Author: MiYoShi8225 <down8225@gmail.com>
Date:   Sat Jun 26 23:16:35 2021 +0900

    cmdの情報を変更

commit 88b21f98c0dbfff29e96af1d50f93ccd3025d925
Author: MiYoShi8225 <down8225@gmail.com>
Date:   Sat Jun 26 23:11:25 2021 +0900

    initial commit
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % 
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git log --oneline
ad3daf6 (HEAD -> master) git diffの情報を追加
81cd31a cmd 情報にstatusの情報を追加
1c1391f cmdの情報を変更
88b21f9 initial commit

```
