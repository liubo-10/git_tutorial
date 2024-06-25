# git笔记

* 👋 Hi, I’m liubo
* 👀 I’m interested in harmony
* 🌱 I’m currently learning harmony
* 💞️ I’m looking to collaborate on ...
* 📫 How to reach me ...



## git设置文件

```shell
Host gitlab
HostName git.zerozero.cn
User liubo00
IdentityFile /home/liubo/00-liubo/my_project/git_config/id_rsa

Host github.com
HostName github.com
User liubo
IdentityFile /home/liubo/00-liubo/my_project/git_config/github_rsa
```

### 添加配置项

git config --file /home/liubo/00-liubo/my_project/git_config/.gitconfig  user.name  "liubo00"
git config --file /home/liubo/00-liubo/my_project/git_config/.gitconfig  user.email "liubo@zerozero.cn"

git config --global user.name  "liubo00"
git config --global user.email "liubo@zerozero.cn"

## 分支管理

### 查看分支

查看分支远端网址

git remote -v

查看远程分支

git branch -r

---

### 更新分支

清理本地不存在的远程分支，如别人删除了dev,但是你本地查看还有，就可以执行该条命令
git remote prune origin

git 更新远程分支列表
git remote update origin --prune



### 删除分支

删除本地分支

git branch -d [branchname]

删除远程分支ulog

方法一
git push origin --delete [branchname]

方法二
git branch -d -r  //删除远程分支，删除后还需推送到服务器
git push origin:   //删除后推送至服务器





git branch -D  liubo/find_device
git branch -D   liubo/find_device_hot

git branch -D  liubo/lock_people_new

git branch -D   liubo/release-v7.0_find_device
git branch -D     liubo/release-v7.0_vio_error
git branch -D    liubo/release-v7_find_device
git branch -D    liubo/vio_error





### 重命名远程分支

git branch -m   //重命名本地分支
git branch -m    old_branch      new_branch
要推动当前分支并将远端设置为上游，使用 ：
git push --set-upstream origin feature/file

## 合并

```bash
git  cherry-pick  a28a8ec0dcdd5037e9c88b0a11e40c971411c5e8

git branch --set-upstream-to=origin/h130/feature_gold_follow  h130/feature_gold_follow



合并单笔提交
git  cherry-pick  67102e097f632e00bdcbddc451c94e1371d2c012
git  cherry-pick  46d688df27ed79cc56b61ad20660fd325449eb5c

```





## 回退

1. 查看版本号：git log，也可以上代码托管网页上查看history，找到需要回滚的目标版本号
2. 使用“git reset --hard 目标版本号”命令将版本回退
3. 使用“git push -f”提交更改，此时如果用“git push”会报错，因为我们本地库HEAD指向的版本比远程库的要旧，用“git push -f”强制推上去。

回退到远程版本

git reset --hard origin/master



git reset --hard 16202cf6ca45169c2dd72da12fe927b77e954d6b





## .gitignore

.gitignore文件修改后，对于修改涉及的文件一般是无法生效的，原因在于已经被追踪的文件记录在.git的缓存中，需要清除缓存。
 方法如下：

```shell
git rm -r --cached . 
git add . 
git commit -m "*" 
git push
```



## 覆盖掉本地

如果您在本地做了改动，但是又不想保留这些改动，可以使用以下命令强制拉取远程最新代码，覆盖掉本地代码：

```bash
git fetch --all  
git reset --hard origin/<branch>


```



## 合并 commit

```bash
git rebase -i 0b50792fb1da1fd38d6d24669536b8a769c5ca52
git rebase -i 16202cf6ca45169c2dd72da12fe927b77e954d6b
git rebase -i c2e280334dde6090ece6203fc25aa67ad4e5a661


```























---
---
---
---
---
---
---
---
---
---
---
---
---
---
---
---
---
---
---
---



