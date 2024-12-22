- 👋 Hi, I’m liubo
- 👀 I’m interested in harmony
- 🌱 I’m currently learning harmony
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 📇 sssssdsdsdsdsdsdasd
- 🎃 dsdsdsdsdsddfsgdgasd
- 🍺 jyukyuiyuiyuigkasd
- 🍥 fsdfgdsgsdgdgadsa
- ✨xcvxcvxcvxcvdasdaasd
- 🍰dazdsxasxsaxsaasdsa

# git笔记

## git设置文件

```git
git config --global --edit
git config --local --edit
--
--system

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

git config --file ~/.gitconfig   user.name   "liubo00"
git config --file ~/.gitconfig   user.email "liubo@zerozero.cn"

git config --global user.name  "liubo00"
git config --global user.email "liubo@zerozero.cn"

git config --global user.email "liubo@zerozero.cn"
git config --global user.name "liubo"

git config --global user.name '刘卜卜' 
git config --global user.email 'liubojinzhou@sina.cn'











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



```shell
git remote prune origin && git remote update origin --prune
```



## 删除分支

删除本地分支

git branch -d [branchname]

删除远程分支ulog

方法一
git push origin --delete [branchname]

方法二
git branch -d -r  //删除远程分支，删除后还需推送到服务器
git push origin:   //删除后推送至服务器

### 重命名远程分支

git branch -m   //重命名本地分支
git branch -m    old_branch      new_branch
要推动当前分支并将远端设置为上游，使用 ：
git push --set-upstream origin feature/file

## 合并

```git
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



## 查看 Git 的配置信息

#### 1. 查看所有配置项

```bash
git config --list
```

这个命令会显示所有级别（系统级、全局级和本地级）的 Git 配置项。

#### 2. 查看全局配置

```bash
git config --global --list
```





## 合并 commit

```git
git rebase -i 0b50792fb1da1fd38d6d24669536b8a769c5ca52
git rebase -i 16202cf6ca45169c2dd72da12fe927b77e954d6b
git rebase -i c2e280334dde6090ece6203fc25aa67ad4e5a661


git push origin --delete    liubo_10_08_dev_open_debug


  remotes/origin/liubo_10_09_heating_new_test
  remotes/origin/liubo_10_09_hotfix
  remotes/origin/liubo_10_11_99%_test
  remotes/origin/liubo_10_11_add_data_reset
  remotes/origin/liubo_10_11_dev_heating_test
  remotes/origin/liubo_10_11_dev_version_138
  remotes/origin/liubo_10_11_heating_abnormal
  remotes/origin/liubo_10_11_heating_open
  remotes/origin/liubo_10_12_dev_heating_test
  remotes/origin/liubo_10_12_heating_status
  remotes/origin/liubo_10_12_low_power_test
  remotes/origin/liubo_10_13_charging_abnormal
  remotes/origin/liubo_10_13_heating_comm_debug
  remotes/origin/liubo_10_14_USB_modify
  remotes/origin/liubo_10_14_heating_comm_debug
  remotes/origin/liubo_10_14_heating_running_status
  remotes/origin/liubo_10_16_USB_detect_delay_modify
  remotes/origin/liubo_10_16_communicate_modify
  remotes/origin/liubo_10_16_current_test
  remotes/origin/liubo_10_18_test
  remotes/origin/liubo_10_19_alarm_modify
  remotes/origin/liubo_10_21_display_SOC
  remotes/origin/liubo_10_24_SOC_map
  remotes/origin/liubo_10_25_add_alarm_event
  remotes/origin/liubo_10_26_add_alarm_test
  remotes/origin/liubo_10_26_add_charging_sleep_logic



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
