### 第三天

在`/etc/apt`软件源`sources.list`,里面的配置会决定你下载的速度，毕竟默认源都是在国外的，如果想速度快一点就哟换成国内的源

- [清华大学源](https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/)

```
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security main restricted universe multiverse

# 预发布软件源，不建议启用
# deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
```

- 中科大源

```
deb http://mirrors.ustc.edu.cn/ubuntu/ precise-updates main restricted
deb-src http://mirrors.ustc.edu.cn/ubuntu/ precise-updates main restricted
deb http://mirrors.ustc.edu.cn/ubuntu/ precise universe
deb-src http://mirrors.ustc.edu.cn/ubuntu/ precise universe
deb http://mirrors.ustc.edu.cn/ubuntu/ precise-updates universe
deb-src http://mirrors.ustc.edu.cn/ubuntu/ precise-updates universe
deb http://mirrors.ustc.edu.cn/ubuntu/ precise multiverse
deb-src http://mirrors.ustc.edu.cn/ubuntu/ precise multiverse
deb http://mirrors.ustc.edu.cn/ubuntu/ precise-updates multiverse
deb-src http://mirrors.ustc.edu.cn/ubuntu/ precise-updates multiverse
deb http://mirrors.ustc.edu.cn/ubuntu/ precise-backports main restricted universe multiverse
deb-src http://mirrors.ustc.edu.cn/ubuntu/ precise-backports main restricted universe multiverse

deb http://security.ubuntu.com/ubuntu precise-security main restricted
deb-src http://security.ubuntu.com/ubuntu precise-security main restricted
deb http://security.ubuntu.com/ubuntu precise-security universe
deb-src http://security.ubuntu.com/ubuntu precise-security universe
deb http://security.ubuntu.com/ubuntu precise-security multiverse
deb-src http://security.ubuntu.com/ubuntu precise-security multiverse
```

- 搜狐源

```
deb http://mirrors.sohu.com/ubuntu/ precise-updates main restricted
deb-src http://mirrors.sohu.com/ubuntu/ precise-updates main restricted
deb http://mirrors.sohu.com/ubuntu/ precise universe
deb-src http://mirrors.sohu.com/ubuntu/ precise universe
deb http://mirrors.sohu.com/ubuntu/ precise-updates universe
deb-src http://mirrors.sohu.com/ubuntu/ precise-updates universe
deb http://mirrors.sohu.com/ubuntu/ precise multiverse
deb-src http://mirrors.sohu.com/ubuntu/ precise multiverse
deb http://mirrors.sohu.com/ubuntu/ precise-updates multiverse
deb-src http://mirrors.sohu.com/ubuntu/ precise-updates multiverse
deb http://mirrors.sohu.com/ubuntu/ precise-backports main restricted universe multiverse
deb-src http://mirrors.sohu.com/ubuntu/ precise-backports main restricted universe multiverse
```
- 网易源

```
deb http://mirrors.163.com/ubuntu/ precise-updates main restricted
deb-src http://mirrors.163.com/ubuntu/ precise-updates main restricted
deb http://mirrors.163.com/ubuntu/ precise universe
deb-src http://mirrors.163.com/ubuntu/ precise universe
deb http://mirrors.163.com/ubuntu/ precise-updates universe
deb-src http://mirrors.163.com/ubuntu/ precise-updates universe
deb http://mirrors.163.com/ubuntu/ precise multiverse
deb-src http://mirrors.163.com/ubuntu/ precise multiverse
deb http://mirrors.163.com/ubuntu/ precise-updates multiverse
deb-src http://mirrors.163.com/ubuntu/ precise-updates multiverse
deb http://mirrors.163.com/ubuntu/ precise-backports main restricted universe multiverse
deb-src http://mirrors.163.com/ubuntu/ precise-backports main restricted universe multiverse
```
- 阿里云

```
# deb cdrom:[Ubuntu 16.04 LTS _Xenial Xerus_ - Release amd64 (20160420.1)]/ xenial main restricted
deb-src http://archive.ubuntu.com/ubuntu xenial main restricted #Added by software-properties
deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted
deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted multiverse universe #Added by software-properties
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted multiverse universe #Added by software-properties
deb http://mirrors.aliyun.com/ubuntu/ xenial universe
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates universe
deb http://mirrors.aliyun.com/ubuntu/ xenial multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse #Added by software-properties
deb http://archive.canonical.com/ubuntu xenial partner
deb-src http://archive.canonical.com/ubuntu xenial partner
deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted multiverse universe #Added by software-properties
deb http://mirrors.aliyun.com/ubuntu/ xenial-security universe
deb http://mirrors.aliyun.com/ubuntu/ xenial-security multiverse
```
然后，大家可以像我这样，来做好备份，有时候，会因为网络问题，需要用到不同的源，好切换！
```
/etc/apt/sources.list （比如，这是官方的源）
/etc/apt/sources.list.qinghua （比如，这是清华的源）
/etc/apt/s ources.list.zhongkeda （比如，这是中科大的源）
/etc/apt/sources.list.sohu （比如，这是搜狐的源）
/etc/apt/sources.list.wangyi （比如，这是网易的源）
```
然后，需要用到哪个了，在比如，我需要用到清华源，则，
```
mv  sources.list.qinghua    sources.list
```
然后，把官方的源，暂时改为
```
mv sources.list   sources.list.bak  
```
配置好了之后要先执行一遍命令`sudo apt-get update`


| 命令     | 含义     |
| :------------- | :------------- |
|  #      | 单行注释代码       |
|`````` xxx ``` ``` | 多行注释       |
| #conding=utf-8 |文件首行，告诉机器使用那种编码        |
|#-*- conding:utf-8 -*-  |  文件首行，告诉机器文件编码(推荐此种) |
|      |        |
|      |        |
|      |        |
|      |        |

#### Python简介

`Python` 的创始人为荷兰人吉多·范罗苏姆（Guido van Rossum）。1989年的圣诞节期间，吉多·范罗苏姆为了在阿姆斯特丹打发时间，决心开发一个新的脚本解释程序，作为 ABC 语言的一种继承。之所以选中 Python 作为程序的名字，是因为他是 BBC 电视剧——蒙提·派森的飞行马戏团（Monty Python's Flying Circus）的爱好者。

#### 第一个Python程序
```
print "hello world!"
```
文件后缀为.py格式

使用命令`python xxx.py`即可运行输出效果

#### 数据类型

![](http://omvbl46i3.bkt.clouddn.com/c201e26d8f4d6b73b9704f0ceef8efe4.png)

#### 变量
定义一个变量，用来存储某一个数值
```
score = 100
```
#### input
表示键盘输入
high = input("请输入你的密码:")

#### print
```
age=18
print("age变量的值%d"%age)
```
```
name="itgoyo"
print("名字是:%s"%name)
```
```
#使用input获取必要的信息
name=input("请输入名字:")

#使用print打印名片
print("==========")
print("姓名:%s"%name)
print("==========")
```
```
name="itgoyo"
age=27
addr="广西"

print("姓名是:%s，年龄是:%d",地址是:%s"%(name,age,addr))
```
#### python3版本中
没有raw_input()函数。只有input

并且python3中的input与python2中的raw_input()功能一样

#### 判断语句

##### if用来完成判断
```
if 条件:
  条件成立的时候，做的事情

```
```
age=19
if age>18:
    print("已经成年，可以去网吧")
else:
    print("未成年，回家写作业吧")
```
#### 提示符的规则
- 提示符由字母、下划线和数字组成，且数字不能开头

#### 关键字
```
import keyword
keyword.klist
```
![](http://omvbl46i3.bkt.clouddn.com/88a12d260044cdd5e199a75ec5829abb.png)
