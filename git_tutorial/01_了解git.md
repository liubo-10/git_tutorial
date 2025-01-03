* 👋 Hi, I’m liubo
* 👀 I’m interested in harmony
* 🌱 I’m currently learning harmony
* 💞️ I’m looking to collaborate on ...
* 📫 How to reach me ...

# 了解Git

Git是一个免费的、开源的分布式版本控制系统，可以高速处理从小型到大型的各种项目
版本控制：是一种记录文件内容变化，以便将来查阅特定版本修订情况的系统

集中式与分布式版本控制工具：

- 集中式版本控制工具：如CVS、SVN等，都有一个单一的几种管理服务器，保存所有文件的修订版本，而协同工作的人通过客户端连接到这台服务器，从而取出最新的文件或者提交更新。缺点：中央服务器的单点故障；多(程序员)对一(中央服务器)

- 分布式版本控制工具：如git,客户端取的不是最新的文件快照，而是把代码仓库完整的镜像下来到本地库(克隆/备份)

Git有最优的存储能力以及非凡的性能，得益于林纳斯（Linus Torvalds一般指林纳斯·本纳第克特·托瓦兹，Linux内核的发明人）本身的这个技能，他是Linux内核专家，也是文件系统的管理专家。所以他开发出来的Git具备了最优的存储能力以及非凡的性能。林纳斯它本身就是崇尚开源的，所以他开发的Git也是开源的。

Git还很容易做备份，还支持离线的操作。基于Git的分支管理的成本是非常低的，而且也非常容易定制工作流程，Git具有这么多的优点，赶快来学习一下Git吧。

工作机制：

![](/home/liubo/00-liubo/learning/git_tutorial/picture/git工作机制.png)

#### Git具有以下特点：

- Git中每个克隆(clone)的版本库都是平等的。你可以从任何一个版本库的克隆来创建属于你自己的版本库，同时你的版本库也可以作为源提供给他人，只要你愿意。
- Git的每一次提取操作，实际上都是一次对代码仓库的完整备份。
- 提交完全在本地完成，无须别人给你授权，你的版本库你作主，并且提交总是会成功。
- 甚至基于旧版本的改动也可以成功提交，提交会基于旧的版本创建一个新的分支。
- Git的提交不会被打断，直到你的工作完全满意了，PUSH给他人或者他人PULL你的版本库，合并会发生在PULL和PUSH过程中，不能自动解决的冲突会提示您手工完成。
- 冲突解决不再像是SVN一样的提交竞赛，而是在需要的时候才进行合并和冲突解决。
- Git 也可以模拟集中式的工作模式
- Git版本库统一放在服务器中
- 可以为 Git 版本库进行授权：谁能创建版本库，谁能向版本库PUSH，谁能够读取（克隆）版本库
- 团队的成员先将服务器的版本库克隆到本地；并经常的从服务器的版本库拉（PULL）最新的更新；
- 团队的成员将自己的改动推（PUSH）到服务器的版本库中，当其他人和版本库同步（PULL）时，会自动获取改变
- Git 的集中式工作模式非常灵活
- 你完全可以在脱离Git服务器所在网络的情况下，如移动办公／出差时，照常使用代码库
- 你只需要在能够接入Git服务器所在网络时，PULL和PUSH即可完成和服务器同步以及提交
- Git提供 rebase 命令，可以让你的改动看起来是基于最新的代码实现的改动
- Git 有更多的工作模式可以选择，远非 Subversion可比

### 3、Git在项目协作开发是解决的问题

1. 多人协作，出现代码冲突 （版本控制工具）
2. 多人协作，在代码整合期间引发BUG（回滚）
3. 多人协作，领导要看项目 （版本历史）
4. 多人协作，用户身份的控制（权限管理）
5. 项目版本的发布问题 （标志&里程碑管理）

2.2.2 设置用户签名 

```shell
git config --global user.name  Tom            #设置用户签名
git config --global user.email 123456@qq.com  #设置用户邮箱
```

只需要首次配置就好了,如何查看配置成功，根据下面路径查看对应文件夹显示即可：

/home/Tom/.gitconfig

——————————————————

版权声明：

本文引用了博主原创文章，著作权归作者所有。遵循 CC 4.0 BY-SA 版权协议，商业转载请联系作者获得授权，非商业转载请附上原文出处链接和本声明。

参考：

链接：https://blog.csdn.net/qq_45796592/article/details/128953729

链接：https://www.jianshu.com/p/c99588857f84

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
