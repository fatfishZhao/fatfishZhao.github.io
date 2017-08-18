---
layout: post
title: "jekyll使用-1"
description: "the first class of using jekyll on Github"
categories: [jekyll]
tags: [blog]
redirect_from:
  - /2017/08/18/
---
# Github创建个人博客
1. 建立一个仓库，名字是username.github.io，并默认加入readme
2. 在settings中随便选择一个theme  
* 可选操作  
3. 在Custom domain输入自己的域名，Github会在项目中生成一个CNAME文件，其中就是自己的域名
4. 在自己的域名解析处进行两个设置
   * 设置记录类型A，主机记录@，记录值为通过ping得到的github.io的ip
   * 设置一个记录类型CNAME，主机记录为www，记录值为username.github.io

# jekyll的使用
### jekyll环境搭建
Windows下的jekyll环境搭建参考[jekyll官网](https://jekyllrb.com/docs/windows/)
1. 下载[RubyInstaller](https://rubyinstaller.org/)并安装
2. 在Windows命令行中，安装jekyll和bundler环境  
   `gem install jekyll bundler`
   
### jekyll主题使用
1. 在[jekyllThemes](http://jekyllthemes.org/)下载主题包
2. 在解压后的主题包中，运行`bundle install`
3. 运行`bundle exec jekyll server`在本地启动jekyll
