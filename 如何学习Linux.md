#如何学习Linux

##学习使用Linux
###主要是要学会基本的命令
>现在开始学习基本的命令，以Linux pocket guide这本书为教材，主要完成以下工作：  
>1. 确定一些基本的命令，以及学要学习的参数。  
>2. 学会这些命令及参数。  
>3. 多重复练习这些参数。  

####Basic File Operations

Command|Options|
------|----|
ls|-a -l -d -F -i -s -R|
cp|-p -a -r -f -i|
mv| -i -f|
rm|-i -f -r
ln|-s -i -f -d

####Directory Operations

Command|Options
------|-------
cd|
pwd|
basename|If you provide an optional suffix, it gets stripped from the result.
dirname|
mkdir|-p -m
rmdir|-p

####File Viewing
Command|Options
-------|-------
cat|-T -E  -v -n -b -s
less|-c -m -N -r -s -S

###学会shell
>这个任务的主要目的是：  
>~~1. 学习记忆bash的主要功能及使用方法。~~  
>~~2. 学习shell的内置命令。~~  
>3. 学习正则表达式，并且总结。

###学会find
>认真学习一些常用的功能。

###学会grep awk
>针对awk有《The awk programming Language》一书。

###学会使用Emacs
>稍微还是有点麻烦与难度的。

##学习配置Linux
###学会各种服务配置
>对于各种服务都配置一次

##学习理解Linux
###学习理解Linux的运行原理

###学习理解Linux的内核原理

##学习玩转Linux
###学习Linux平台的编程