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

## git diff について

```sh
git addする前の変更分
# git diff
# git diff <ファイル名>


git addした後野変更分
# git diff --staged
```

## git log について

- git のログ情報を確認するコマンド

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

## git rm

- ファイル削除を行うコマンドについて

```sh
gitからもローカルからも情報を削除するコマンド
# git rm <ファイル名>
# git rm -r <フォルダ名>


ファイルを残したいとき(ローカルには残してgitの情報から削除する方法)
# git -rm --cached <ファイル名>

リポジトリ情報の復活↓
# git reset HEAD index.html

ファイルの復活↓
git checkout index.html
```

```sh
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git rm index.html
rm 'index.html'
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	deleted:    index.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   git_cmd.md

(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git reset HEAD index.html
Unstaged changes after reset:
M	git_cmd.md
D	index.html
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git checkout index.html
Updated 1 path from the index
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % ls
git_cmd.md	index.html
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   git_cmd.md

no changes added to commit (use "git add" and/or "git commit -a")
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git rm --cached index.html
rm 'index.html'
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % ls
git_cmd.md	index.html
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % echo ある！
ある！
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	deleted:    index.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   git_cmd.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	index.html

(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git reset HEAD index.html
Unstaged changes after reset:
M	git_cmd.md
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   git_cmd.md

no changes added to commit (use "git add" and/or "git commit -a")
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git commit
On branch master
Changes not staged for commit:
	modified:   git_cmd.md

no changes added to commit
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git add .
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git commit
[master 727db4c] git rm cmdを使った実習
 1 file changed, 34 insertions(+)
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %
```

## git mv について

- git でのファイル名の変更やディレクトリ移動を行うもの

```sh
# git mv <前ファイル名> <後ファイル名>

以下のコマンドと同じ
# mv <前ファイル名> <後ファイル名>
# git rm <前フォルダ>
# git add <後フォルダ>
```

## gitHub にアップする

```sh
リモートリポジトリを新規追加する
# git remote add origin <githubURL>

リモートリポジトリへ情報を送信する
# git push <リモート名><ブランチ名>

↓で次回以降は[git push]だけでいいらしい(もしかしたら古いかも今はやらなくても使える可能性あり)
# git push -u origin master
```

```sh
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % {
cursh> git remote add origin https://github.com/MiYoShi8225/git_tutorial.git
cursh> }
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git push -u origin master
Enumerating objects: 25, done.
Counting objects: 100% (25/25), done.
Delta compression using up to 8 threads
Compressing objects: 100% (24/24), done.
Writing objects: 100% (25/25), 3.95 KiB | 1011.00 KiB/s, done.
Total 25 (delta 7), reused 0 (delta 0)
remote: Resolving deltas: 100% (7/7), done.
To https://github.com/MiYoShi8225/git_tutorial.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %

```

##

- パスワードの情報や team 開発で必要ないファイル、フォルダを git 情報に加えない方法
  - .gitignor を編集する

```sh

ignoreファイルを作成してそこにファイル名(相対パス)を記載するとそのファイルはgitに情報として追加されない
# touch .gitignore
# vi .gitignore

# vi中
# <ファイル名を追加>

```

```sh
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   git_cmd.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        secret.txt

no changes added to commit (use "git add" and/or "git commit -a")
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %

# ↑は.gitignoreがない状態
# ↓は.gitignoreにsecret.txtを記載した状態

(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   git_cmd.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

no changes added to commit (use "git add" and/or "git commit -a")
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %
```
fffff