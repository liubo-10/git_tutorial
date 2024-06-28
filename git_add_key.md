* 👋 Hi, I’m liubo
* 👀 I’m interested in harmony
* 🌱 I’m currently learning harmony
* 💞️ I’m looking to collaborate on ...
* 📫 How to reach me ...

# git 密钥



## 启用密钥快速命令

```shell
ssh-add /home/liubo/00-liubo/my_material/my_note/git/git_key/gitlab_rsa && 

ssh-add /home/liubo/00-liubo/my_material/my_note/git/git_key/github_rsa
```

## 添加密钥gitlab(zerozero)

生成密钥

```shell=
ssh-keygen -t rsa -C liubo@zerozero.cn
```



添加密钥，网页添加

https://git.zerozero.cn/profile/keys



启用密钥

```shell
#linux
密钥路径
/home/liubo/00-liubo/my_material/my_note/git/git_key
启用密钥
ssh-add /home/liubo/00-liubo/my_material/my_note/git/git_key/gitlab_rsa

#141服务器
/home/liubo/git/git_key/id_rsa
启用密钥
eval $(ssh-agent -s)
ssh-add /home/liubo/git/git_key/id_rsa

#windows
密钥路径
/e/my_tool/git_key/gitlab_rsa
启用密钥
eval $(ssh-agent -s)
ssh-add  /e/my_tool/git_key/gitlab_rsa

#wiondows虚拟机
密钥路径
/c/00_liubo/git_key/id_rsa
启用密钥
eval $(ssh-agent -s)
ssh-add /c/00_liubo/git_key/id_rsa

```

测试密钥

```shell
ssh -T  git@git.zerozero.cn
```

## 添加密钥github(liubo-10)



生成密钥

```shell
ssh-keygen -t rsa -C liubojinzhou@sina.cn
```

添加密钥，网页添加

https://github.com/settings/keys



```shell
#linux
密钥路径
/home/liubo/00-liubo/my_material/my_note/git/git_key
启用密钥
ssh-add /home/liubo/00-liubo/my_material/my_note/git/git_key/github_rsa


#windows
密钥路径
/e/my_tool/git_key/github_rsa
启用密钥
eval $(ssh-agent -s)
ssh-add  /e/my_tool/git_key/github_rsa
```



测试密钥

```shell
ssh -T git@github.com
```



## 添加密钥gitee(bliu2_10)

### windows

生成密钥

```shell
ssh-keygen -t rsa -C liubojinzhou@sina.cn
```

密钥路径

```shell
/e/my_note/git/git_key/gitee_rsa
```

添加密钥，网页添加

https://gitee.com/profile/sshkeys





启用密钥

```shell
ssh-agent bash  //添加不了，运行这个命令
ssh-add    /e/my_note/git/git_key/gitee_rsa

git config --global user.name '刘卜卜' 
git config --global user.email 'liubojinzhou@sina.cn'
```

测试密钥

```shell
ssh -T git@gitee.com
```



### linux



生成密钥

```shell
ssh-keygen -t rsa -C liubojinzhou@sina.cn
```

密钥路径

```shell
/home/liubo/00-liubo/my_material/my_note/git/git_key/gitee_linux_rsa
```

添加密钥，网页添加

https://gitee.com/profile/sshkeys



启用密钥

```shell
ssh-add /home/liubo/00-liubo/my_material/my_note/git/git_key/gitee_linux_rsa
```

测试密钥

```shell
ssh -T git@gitee.com
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
