---
layout: post
title: "远程使用ipython notebook、tensorboard"
description: "using ipython notebook and tensorboard remotely"
categories: [python,tensorflow]
tags: [blog]
redirect_from:
  - /2017/09/22/
---
# 利用Ubuntu的Anaconda实现远程访问服务器ipython notebook
1. 在服务器端安装好anaconda
2. 在个人电脑有ssh服务，我目前用的是git的bash终端
3. 在服务器执行以下命令  
	`jupyter notebook --no-browser --port=7001`  
	将会创建一个没有浏览器的notebook，指定端口为7001
4. 在个人电脑的终端，输入  
	`ssh -N -f -L localhost:7002:localhost:7001 username@remote.computer.name`  
	在浏览器中打开远程终端显示的url，将7001改成7002即可
## 相关链接：
[Remote Access to IPython Notebooks via SSH](https://coderwall.com/p/ohk6cg/remote-access-to-ipython-notebooks-via-ssh)  
[connect to ipython jupyter notebook hosted remotely using your own browser](https://www.youtube.com/watch?v=J91RhThcrN4)

# 远程访问tensorboard
1. 在server的终端输入`tensorboard --logdir='logs/'`启动tensorboard
2. 在windows端输入`ssh -L 16006:127.0.0.1:6006 username@remote.computer.name`
3. 在本地打开127.0.0.1:16006即可