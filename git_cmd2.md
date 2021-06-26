# git cmd2

## git checkout について

- ファイルへの変更を取り消す方法
  - ステージ(add した情報)をもとにファイルの情報修正を行う

```sh
# git checkout -- <ファイル名>
# git checkout -- <フォルダ名>

全体の変更を取り消す
# git checkout -- .

--はブランチ名とファイル名がかぶった時にわかりやすくするために
```

```sh
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   git_cmd2.md

no changes added to commit (use "git add" and/or "git commit -a")
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git checkout -- git_cmd2.md
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial %
```

## git reset HEAD

- stage に変更した情報を取り消す
  - 指定した変更をステージから取り消すだけなので、ワークツリーのファイルには影響がない
  - かんたんに言えば stage の情報を消すよ！(前回 commit した情報から逆算して)

```sh
# git reset HEAD <ファイル名>
# git reset HEAD <フォルダ名>

すべて変更を取り消す
# git reset HEAD .
```

## git commit --amend

- 直前の commit を修正することができる
  - リモートリポジトリに push した情報に対して直前の commit 修正は行っては行けない！！

```sh

# git commit --amend
```
