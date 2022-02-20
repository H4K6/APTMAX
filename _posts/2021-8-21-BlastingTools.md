---
title: 验证码爆破工具
author: APT - 0x44LL
date: 2021-01-17
category: 0x44LL
layout: post
---

# 验证码爆破工具 - Blasting Tools

## 该工具在原作者的基础上进行了优化了逻辑并加强了OCR识别能力，验证码识别能力大幅度提升，识别准确率极高。

# 识别测试栏

url获取 右键验证码图片-复制图片地址

放入验证码url地址点击 **识别**

![](/public/DocsPics/Blasting-tools/Blasting-tools1.png)

# 请求栏

1. 复制登陆请求包到框内【POST GET都可】
2. 复制验证码地址到框内
3. 添加标记【这里的标记用于账号或者密码】
4. 添加验证码标记【这里的标记用于验证码】
5. 选择账号或者密码爆破【标记的啥选啥】
6. 导入【标记的啥导入啥】
7. 注意:验证码同步不要关闭,勾选了不要去管他！

![](/public/DocsPics/Blasting-tools/Blasting-tools2.png)

# 爆破栏

1. 选择爆破栏，填入爆破后台的url地址
2. 设置好错误页线程
3. 设置好线程
4. 启用代理（建议调用随机ip代理）


![](/public/DocsPics/Blasting-tools/Blasting-tools3.png)

点击Start 就会开始爆破。验证码也会自动识别。

# 加密数据爆破

右键-检查-对应参数

填写对应参数

![](/public/DocsPics/Blasting-tools/Blasting-tools4.png)

![](/public/DocsPics/Blasting-tools/Blasting-tools5.png)

抓登入包

返回特征：

{&quot;success&quot;:false,&quot; message&quot;:&quot;CHECK\_CODE&quot;}

![](/public/DocsPics/Blasting-tools/Blasting-tools6.png)

![](/public/DocsPics/Blasting-tools/Blasting-tools7.png)

开始爆破

# 实战用例

御剑进行扫描

![](/public/DocsPics/Blasting-tools/Blasting-tools8.png)

发现敏感路径及后台

文章中得知发布者用户名有 **admin**

![](/public/DocsPics/Blasting-tools/Blasting-tools9.png)

![](/public/DocsPics/Blasting-tools/Blasting-tools10.png)

进行抓登入包及密码导入工具中

![](/public/DocsPics/Blasting-tools/Blasting-tools11.png)

PS：点击序号，状态码，相应长度可进行升降排序，单机某栏，可查看请求包与相应包内容!

![](/public/DocsPics/Blasting-tools/Blasting-tools12.png)

爆破到密码

![](/public/DocsPics/Blasting-tools/Blasting-tools13.png)

爆破密码登入成功！