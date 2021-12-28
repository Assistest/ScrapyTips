# ScrapyTips
为你的Scrapy开启代码提示，可能会让你觉得更好用。

# 前言
1. 你是一个很好的框架Scrapy。

# Scrapy

1. github地址：[github地址](https://github.com/scrapy/scrapy)
2. 官方网站：[官方网站](https://scrapy.org/)
3. 官方文档：[官方文档](https://docs.scrapy.org/en/latest/)

# 主要

1. 主要使用类型注解为Scrapy父类指定类型

2. 一些没有继承关系的类型，通过修改模版语法，在创建之初就为其在代码中添加类型注解

   

## 目前已经开启的有

1. 默认回调函数：**Parse，Response，Xpath，Re。**
   1. **用户自定义的回调函数无法操作，请手动按默认回调进行修改。**
2. 管道item：**会提示用户已定义的类型**
3. 媒体管道：**（图片下载管道，文件下载管道）**
4. 中间件：**crawler，spider，request，response，start_requests，result**
   1. 中间件的**exception**：就算指定了类型注解，还是不会出现代码提示
   2. 但直接对对象调用，却可以出现，这个问题有了解的请留言。
5. 已默认将日志等级改为：**ERROR**。

## 安装

1. 修改的是Scrapy2.5.1
2. 你可以通过 `scrapy install scrapy==2.5.1` 进行安装
3. 之后下载压缩包,将内部的所有文件，替换到Python安装目录：`Python\Python38\Lib\site-packages\scrapy`
4. **之后需要重新创建一个项目才可以开启中间件和管道的提示，否则只有回调函数提示。**

# 最后
1. 如果你有更好的建议，可以联系我
