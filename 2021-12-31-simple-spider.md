---
layout: post
title: simple spider
tags: 
- python
---

# 爬虫：

header必须要 ctrl + R +正则批量做header

cookie就是一个字符串从浏览器请求里面抄，

### lxml etree真好用 建立一个`etree.HTML(string)`建一个对象，用obj.xpath在里面找路径就完事了

#### 谓语

- and与操作`//a[@name="lining" and @age="22"]`，同理or，not(...)
- 判断有没有属性`//a[@name]`存在name属性
- 获得标签内文本`//a/text()`

常用xpath：

- // 在所有可能位置寻找  / 在根开始
- //script + //script[@id="ta de id"]

### scrapy

scrapy startproject name 建一个

注意parse函数返回的结果都是Item类型或者**字典**，如果返回一列数据，用yield

scrapy shell "https://www.lagou.com/wn/" --nolog， 用这个shell写xpath语句，**定位数据**啥的

定义spider时给他一个全局的名字。使用scrapy.Request(url, callback)来创建请求，返回html response啥的给回调函数，**回调函数发给pipeline**。不要返回列表！！

爬虫经典问题就是字符编码的问题，看返回的charset，注意使用utf-8对二进制编码。使用框架没这问题。

### 读写文件

没想到这时候还能被它坑了

r+ 读文件之后能写文件，注意读了后文件指针移动到文件末尾，此时写文件double，`f.seek(0, os.SEEK_SET)`将指针移到开始

w+是先写后读，**先把文件内容清空**，然后写读结合，不能用

