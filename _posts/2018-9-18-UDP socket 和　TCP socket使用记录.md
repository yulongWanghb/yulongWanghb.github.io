---
layout:     post
title:     
subtitle:   socket 在不同协议下的封装
date:       2018.0９.18
author:     WYL
catalog: true
tags:
    - socket
---
#### 创建socket
int socket(int domain, int type,int protocal);
成功 ：返回新创建的socket 的****文件描述符****
失败：返回-1 ，设置errno
注意使用的是TCP还是UDP协议

细节参考[Linux socket](https://blog.csdn.net/qq_35426012/article/details/72598949)


#### fcntl函数的使用     
fcntl函数用于对（文件）描述符提供控制，3种构造函数    
**返回值**:1. 函数出错，所有命令返回值都是-1，成功的话返回某个其他值
细节参考[fcntl详细使用](https://www.cnblogs.com/xuyh/p/3273082.html)

#### setsockopt 函数
函数功能描述：
设置连接的一些参数，同时在失败的时候设置errno的值为对应的状态码
细节参考[setsockopt详细使用](https://www.cnblogs.com/eeexu123/p/5275783.html)

#### 异步套接字
