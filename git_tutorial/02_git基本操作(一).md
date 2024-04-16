* 👋 Hi, I’m liubo
* 👀 I’m interested in harmony
* 🌱 I’m currently learning harmony
* 💞️ I’m looking to collaborate on ...
* 📫 How to reach me ...



# git基本操作

本文讲解 git 的几种基本操作

# 1、git init

初始化本地仓库

要对现有的某个项目开始使用Git管理，只需到此项目所在的主目录，执行命令 git init 即可。

比如 ~/00-liubo/learning/Git_test 为某个项目主目录

```shell
liubo@thinkpad:~/00-liubo/learning/Git_test$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint:   git config --global init.defaultBranch <name>
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint:   git branch -m <name>
Initialised empty Git repository in /home/liubo/00-liubo/learning/Git_test/.git/

liubo@thinkpad:~/00-liubo/learning/Git_test$ ll
total 12
drwxrwxr-x  3 liubo liubo 4096  4月 16 09:49 ./
drwxrwxr-x 11 liubo liubo 4096  4月 15 17:53 ../
drwxrwxr-x  7 liubo liubo 4096  4月 16 09:49 .git/
```

说明：

初始化Git仓库后，在当前目录下会出现一个名为.git的目录，所有Git需要的数据和资源都存放在这个目录中。

不过目前，仅仅是按照既有的结构框架，初始化好了Git仓库中所有的文件和目录，但我们还没有开始跟踪管理项目中的任何一个文件。



## 2、git status

查看文件的状态

进入项目主目录，执行命令 git status 查看工作区、暂存区中文件的状态。

```shell
liubo@thinkpad:~/00-liubo/learning/Git_test$ git status  # 查看工作区、暂存区状态
On branch master  # 在主分支上工作

No commits yet   # 尚无提交文件，指的是本地库中没有提交过任何文件。

# 无需提交（可创建/复制文件并使用“git add”进行跟踪）
# 无需提交指的是，暂存区中没有任何可提交的文件
# 追踪文件，就是让Git管理该文件。
nothing to commit (create/copy files and use "git add" to track)
```

创建文件后查看工作区、暂存区中文件的状态

我们在仓库目录中创建一个readme.txt文件后，在执行git status命令。

```shell
liubo@thinkpad:~/00-liubo/learning/Git_test$ touch readme.txt  # 创建readme.txt文件
liubo@thinkpad:~/00-liubo/learning/Git_test$ ll
总计 12
drwxrwxr-x  3 liubo liubo 4096  4月 15 18:29 ./
drwxrwxr-x 11 liubo liubo 4096  4月 15 17:53 ../
drwxrwxr-x  7 liubo liubo 4096  4月 15 18:25 .git/
-rw-rw-r--  1 liubo liubo    0  4月 15 18:29 readme.txt
```



```shell
liubo@thinkpad:~/00-liubo/learning/Git_test$ git status  # 查看工作区、暂存区状态
On branch master

No commits yet  # 尚无提交文件，指的是本地库中没有提交过任何文件。

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        readme.txt

nothing added to commit but untracked files present (use "git add" to track)
```

说明：

- Untracked files:readme.txt 

  表示发现未追踪的文件readme.txt

- use "git add <file>..." to include in what will be committed

  表示对readme.txt文件，你可以使用git add <file>命令， 将新建文件添加到暂存区。

- nothing added to commit but untracked files present (use "git add" to track)

  表示你没有添加任何内容到暂存区，但是存在未追踪的文件， 可使用“git add”进行追踪。

  

## 3、git add

将工作区的文件添加到暂存区

执行命令 git add ，将readme.txt文件添加到暂存区。

在git add命令后面可以指明要跟踪的文件或目录路径。如果是目录的话，就说明要递归跟踪该目录下的所有文件。（其实git add命令的潜台词就是把目标文件快照放入暂存区域，同时未曾跟踪过的文件标记为已跟踪。

执行命令 git status 再次查看工作区、暂存区状态

```shell
liubo@thinkpad:~/00-liubo/learning/Git_test$ git add readme.txt
liubo@thinkpad:~/00-liubo/learning/Git_test$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   readme.txt

```

说明：

- Changes to be committed: new file: readme.txt 

  所做更改：新建了readme.txt文件

- use "git rm --cached <file>..." to unstage 

  提示你可以适用使“git rm --cached <file> ...”命令，把文件从暂存区中撤回到工作区。

总结：

只要在"Changes to be committed"这行下面显示的文件，就说明是已暂存状态。

如果此时提交，那么该文件此时此刻的版本，将被留存在历史记录中。





## 4、git rm --cached

将文件从暂存区撤回到工作区

执行命令 git rm --cached readme.txt，将readme.txt文件从暂存区撤回到工作区，但不会从物理磁盘中删除该文件。

执行命令 git status 命令查看工作区、暂存区状态。

```shell
liubo@thinkpad:~/00-liubo/learning/Git_test$  git rm --cached readme.txt
rm 'readme.txt'
liubo@thinkpad:~/00-liubo/learning/Git_test$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        readme.txt

nothing added to commit but untracked files present (use "git add" to track)
```

可以看到结果，readme.txt文件又成为了一个未被Git追踪的文件。





——————————————————

版权声明：

本文引用了博主原创文章，著作权归作者所有。遵循 CC 4.0 BY-SA 版权协议，商业转载请联系作者获得授权，非商业转载请附上原文出处链接和本声明。



参考：

链接：https://www.jianshu.com/p/455135b4b8f6
链接：https://blog.csdn.net/qingzhuyuxian/article/details/135941036








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













  
