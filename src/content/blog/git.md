---
title: Git
description: ……
pubDate: 2 13 2025
image: /image/image3.png
categories:
  - tech
tags:
  - git
---

### 配置Git
1.配置本地信息
为了在后面上传项目到github时方便知道是谁上传的，需要给本机git配置用户名和邮箱：

git config --global user.name "Your Name"
git config --global user.email "email@example.com"

打开 git bash（也可任意位置右键打开 git bash）：

查看配置命令：git config --list

2.配置SSH
1）SSH与SSH Key是什么？
要了解SSH key简介，首先得熟悉SSH，Secure Shell (SSH) 是一个允许两台电脑之间通过安全的连接进行数据交换的网络协议。SSH 密钥对可以让您方便的登录到 SSH 服务器，而无需输入密码。SSH 密钥对总是成双出现的，一把公钥，一把私钥。这里用到了非对称公钥加密体系，生成的公钥放到github的网站上，生成的私钥放在自己的电脑上。

2）生成SSH Key

ssh-kygen -t rsa -C “注册邮箱”

//执行后一直回车即可

3）获取ssh key公钥内容（id_rsa.pub）
cd ~/.ssh
cat id_rsa.pub



4）Github账号上添加公钥
进入Settings设置

添加ssh key，把刚才复制的内容粘贴上去保存即可



5）验证是否配置成功
ssh -T git@github.com

————————————————

```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin 仓库地址
git push -u origin main
```

