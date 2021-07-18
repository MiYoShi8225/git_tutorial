
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


