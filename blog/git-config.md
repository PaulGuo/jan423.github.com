# 读《Git权威指南》有感——配置篇

以下所有信息都是我从《Git权威指南》获取到的知识——Jan

## 配置的作用域

	git config  xxxx
	git config --global xxxx
	git config --system xxxx

三个参数（null，global，system）分别对应于版本库，用户级别，系统级别。

## 配置别名
	
	//为用户级别config配置一个别名
	git config --global alias.conf "config --global"
	//打开显示颜色
	git conf color.ui true
	//配置你的姓名
	git conf user.name "yingyi.zj"
	//配置你的邮箱
	git conf user.email "xxx.xxx"
	//配置一些简单的别名demo
	git conf alias.st status
	git conf alias.br branch
	git conf alias.com "commit -am"
	git conf alias.ch checkout

## Log命令的一些配置
	
### 参数
	--graph 图形显示log
	--oneline 单行显示log
	--raw 原生的log信息显示

###alias

	git conf alias.lo "log --graph --raw"


## 信息摘要

一个算法，可以将任意长度的信息转换为固定长度输出，并且对不同信息的摘要唯一。目前比较著名的实现算法有MD5与SHA1。当然转换后的信息重复的概率很小。

在git中摘要是对commit，blob和tree进行SHA1。

其实理解了git的原理很容易玩转git的。

## reset 和reflog

reset是将以前的commit恢复到工作区或者缓冲区

reflog是利用log文件将commit恢复到日志中某个状态

### reset
	//soft只改变commit对象
	//mixed只commit、暂存区而不改变工作区，默认为这个参数
	//hard改变所有区域
	git reset [--soft | --mixed | --hard ] [<commit>]
	git reset HEAD
	git reset HEAD^^

### reflog

	git reset [--soft | --mixed | --hard ] [<commit>]
	//改变当前工作区，缓冲区，commit到master的第三个状态
	git reset --hard master@{3}