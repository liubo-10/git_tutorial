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



# gitlab(zerozero)

## 生成密钥

```shell=
ssh-keygen -t rsa -C liubo@zerozero.cn
```

## 密钥路径

```
linux主机
/home/liubo/00-liubo/my_material/my_note/git/git_key

141服务器
/home/liubo/git/git_key/id_rsa

wiondows
/e/my_tool/git_key/gitlab_rsa
```

## 密钥添加网页

网址

[Sign in · GitLab](https://git.zerozero.cn/profile/keys)

## 启用密钥

```shell
👋linux主机
ssh-add /home/liubo/00-liubo/my_material/my_note/git/git_key/gitlab_rsa

👋141服务器
eval $(ssh-agent -s)
ssh-add /home/liubo/git/git_key/id_rsa

👋wiondows虚拟机
eval $(ssh-agent -s)
ssh-add /c/00_liubo/git_key/id_rsa

👋wiondows
eval $(ssh-agent -s)
ssh-add /e/my_tool/git_key/gitlab_rsa
```

## 测试密钥

```shell
ssh -T  git@git.zerozero.cn
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
