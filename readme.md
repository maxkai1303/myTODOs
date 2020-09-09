### maxkai@MaxdeMacBook-Pro ~ % cd Desktop 

### maxkai@MaxdeMacBook-Pro Desktop % cd myTODOs 

### maxkai@MaxdeMacBook-Pro myTODOs % git status

`On branch master`
`nothing to commit, working tree clean`


### maxkai@MaxdeMacBook-Pro myTODOs % git commit -m "first"
`On branch master`
`nothing to commit, working tree clean`

###### 在這邊發現我資料夾裡面沒有資料可以commit

### maxkai@MaxdeMacBook-Pro myTODOs % vim REDEME.html
### maxkai@MaxdeMacBook-Pro myTODOs % git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

    REDEME.html

nothing added to commit but untracked files present (use "git add" to track)

###### 新增一個檔案讓他有東西可以commit


### maxkai@MaxdeMacBook-Pro myTODOs % git commit -m "first"
On branch master
Untracked files:
    REDEME.html

nothing added to commit but untracked files present

###### 發現我忘了先add那個文件

### maxkai@MaxdeMacBook-Pro myTODOs % git add REDEME.html 
### maxkai@MaxdeMacBook-Pro myTODOs % git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

    new file:   REDEME.html

### maxkai@MaxdeMacBook-Pro myTODOs % git commit -m "first"
###### 這裡要記得一定要順便-m"message"
[master 9a5edfc] first
 1 file changed, 2 insertions(+)
 create mode 100644 REDEME.html
 
 ### maxkai@MaxdeMacBook-Pro myTODOs % git branch -m master
 ### maxkai@MaxdeMacBook-Pro myTODOs % git remote add origin https://github.com/maxkai1303/myTODOs.git
`fatal: remote origin already exists.`

###### 失敗了他說origin這個遠程分支已經存在了，所以現在要來把它刪掉重建

### maxkai@MaxdeMacBook-Pro myTODOs % git remote rm origin
### maxkai@MaxdeMacBook-Pro myTODOs % git remote add origin fatal: remote origin already exists.
usage: git remote add [<options>] <name> <url>

    -f, --fetch           fetch the remote branches
    --tags                import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --track <branch>  branch(es) to track
    -m, --master <branch>
                          master branch
    --mirror[=<push|fetch>]
                          set up remote as a mirror to push to or fetch from

#### maxkai@MaxdeMacBook-Pro myTODOs % git remote rm origin
`fatal: No such remote: origin`

###### 再確認一次確實刪掉了origin

### maxkai@MaxdeMacBook-Pro myTODOs % git remote add origin https://github.com/maxkai1303/myTODOs.git
### maxkai@MaxdeMacBook-Pro myTODOs % git push -u origin master

    Counting objects: 9, done.
    Delta compression using up to 8 threads.
    Compressing objects: 100% (6/6), done.
    Writing objects: 100% (9/9), 1.37 KiB | 1.37 MiB/s, done.
    Total 9 (delta 0), reused 0 (delta 0)
    To https://github.com/maxkai1303/myTODOs.git
     * [new branch]      master -> master
    Branch 'master' set up to track remote branch 'master' from 'origin'.
    
## 用本機資料推上乾淨的GitHub
