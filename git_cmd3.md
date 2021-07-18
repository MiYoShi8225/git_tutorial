
## git remote
```sh

# git remote 


# git remote -v

```

## git fetch
```sh
# git fetch origin
```

## git pull 
- リモートリポジトリーから情報を取ってきてローカルリポジトリに変更を行う
```sh
# git pull <origin> <master>

```

## git remote show

```sh
# git remote show <リモート名>
```

```sh
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git remote show origin
* remote origin
  Fetch URL: https://github.com/MiYoShi8225/git_tutorial.git
  Push  URL: https://github.com/MiYoShi8225/git_tutorial.git
  HEAD branch: master
  Remote branch:
    master tracked
  Local ref configured for 'git push':
    master pushes to master (fast-forwardable)
```

## git remote rename <旧リモート名> <新リモート名>
## git remote rm <リモート名>
```sh
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git remote rename bk bak
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git remote
bak
origin
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git remote rm bak       
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git remote
origin
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % 
```


## git branch
- ブランチを作成する
    - ブランチの切り替えはしないよ

```sh
今あるブランチを表示する
# git branch
# git branch -a

新しくブランチを作成する
# git branch <名前>

ブランチ情報を確認する
# git log --oneline --decorate

```

## git checkout
- ブランチを切り替える

```sh
ブランチを切り替える
# git checkout <ブランチ名>


(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git checkout feature
M       git_cmd3.md
Switched to branch 'feature'
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % git branch
* feature
  master
(base) miyoshishun@miyoshishunnoMacBook-Air git_turorial % 
```


```

作成と切り替えを一緒に行う
# git checkout -b <ブランチ名>
```