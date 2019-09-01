---
layout:     post
title:      "Hello World"
subtitle:   ""
date:       2017-06-17 00:09:00
author:     "陈实"
header-img: ""
catalog: true
tags:
    - 闲扯
---

## 本地调试
- 下载[Ruby+Devkit](https://rubyinstaller.org/downloads/)(我下的是2.6.0)，安装
- gem install jekyll
- gem install jekyll bundler
- 进入博客所在文件夹，jekyll serve
- 在这里 http://127.0.0.1:4000/ 就可以看到博客
### 报错
- jekyll server时报错"The 'gems' configuration option has been renamed to 'plugins'. Please update your configuration file accordingly.".解决：将博客配置文件_config.yml中的gems:改为plugins:，然后gem install jekyll-paginate
