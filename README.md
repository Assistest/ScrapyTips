# ScrapyTips（更新到 2.6.1）

为你的 Scrapy 开启代码提示，可能会让你觉得更好用。



## 22.3.30

1. 增加一个RUN_PATH属性,每次用 相对路径总是会有莫名其妙的问题
2. 修改日志配置，在你指定日志文件之后控制台也会输出
   1. 我就是希望控制台输出的同时，也输出到指定的本地文件
   2. 以注释的形式增加，可以不用解开注释

# 前言

1. 你是一个很好的框架 Scrapy。
2. 每次手动修改都很麻烦，你要是可以集成到你的源码中就好了...Scrapy
3. 增加一个：handle_httpstatus_list = []
   1. 因为我有的时候会需要处理异常,比如 302,404

# Scrapy

1. github 地址：[github 地址](https://github.com/scrapy/scrapy)
2. 官方网站：[官方网站](https://scrapy.org/)
3. 官方文档：[官方文档](https://docs.scrapy.org/en/latest/)

# 主要

1. 全部都改成类型注解

## 开启的有

1. 默认回调函数：**Parse，Response，Xpath，Re。**
   1. **用户自定义的回调函数无法操作，请手动按默认回调进行修改。**
2. 管道 item：**会提示用户已定义的类型**
3. 媒体管道：**（图片下载管道，文件下载管道）**
4. 中间件：**crawler，spider，request，response，start_requests，result**
   1. 中间件的**exception**：就算指定了类型注解，还是不会出现代码提示
   2. 但直接对对象调用，却可以出现，这个问题有了解的请留言。
5. 已默认将日志等级改为：**ERROR**。

## 安装

1. 修改的是 Scrapy2.6.1
2. 你可以通过 `pip install scrapy==2.6.1` 进行安装
3. 之后下载压缩包,将内部的所有文件，替换到 Python 安装目录：`Python\Python38\Lib\site-packages\scrapy`
   1. 这里不一定要 3.8 版本,现在 2.6.1 已经支持 Python3.10.0
4. **之后需要重新创建一个项目才可以开启中间件和管道的提示.**
