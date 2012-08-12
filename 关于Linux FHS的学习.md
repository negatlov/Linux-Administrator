#Learning FHS
>主要参考 Filesystem Hierarchy Standard

##对于Linux绝对路径的理解
实际上linux的绝对路径是由三个部分构成：

1. Scope
2. Category
3. Program

##对于Root Filesystem的理解
###Q1:根目录设计的目的是什么？
为了用于boot, restore, recover, repair系统。即`3RB`功能。
###02:如何才能完成该目的？根文件系统中该有什么?
>对于该问题，在fhs中有详细的解释。

1. To boot a system, enough software and data must be present on the root partition to mount other filesystems. This includes utilities, configuration, boot loader information, and other essential start-up data. **/usr, /opt, and /var** are designed such that they may be located on other partitions or filesystems.  	
2. To enable recovery and/or repair of a system, those utilities needed by an experienced maintainer to diagnose and reconstruct a damaged system must be present on the root filesystem.
3. To restore a system, those utilities needed to restore from system backups (on floppy, tape, etc.) must be present on the root filesystem.

**A**pplications must never create or require special files or subdirectories in the root directory. Other locations in the FHS hierarchy provide more than enough flexibility for any package.

###Q3:该文件系统下有什么目录？
>目前是按照分类的方式记忆的。 

1. Kernel  
/boot 可能包含内核文件、grub等引导程序  
2. Programs  
/bin  
/sbin 用于3RB的程序  
/lib  
/opt  
3. Configuration  
/etc 
4. Hardware  
/dev  
/mnt  临时挂载点   
/media
5. Runtime  
/var  当/usr是只读的时候，该写入/usr的数据都会写入/var  
/tmp  
6. Misc.  
/srv  服务程序的数据保存地。

##对于/Usr目录的分析
该目录和/usr/local的结构基本一致，主要有：  

1. Programs   
	* bin
	* sbin
	* lib
2. Programming  
	* include
	* src
3. Documents  
	* share 与体系无关的数据。
	* man(只存在于/usr/local中，且是/usr/local/share/man的软连接)
4. Game  

##对于/usr/local目录的分析
相比/usr的结构，多了etc目录。**该目录可能是/etc/local的软连接。**

1. Programs   
	* bin
	* sbin
	* lib
2. Programming  
	* include
	* src
3. Documents  
	* share 与体系无关的数据。
	* man(只存在于/usr/local中，且是/usr/local/share/man的软连接)
4. Game  
5. Configuration
	* etc
	
##对于share文件的分析
>主要有man、misc两个文件夹。

Manual pages are stored in `<mandir>/<locale>/man<section>/<arch>`