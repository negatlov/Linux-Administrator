#UNIX&copy; AND LINUX® SYSTEM ADMINISTRATION HANDBOOK

##Chapter 1
###Pg 15.
1. (推荐)关于Linux/Unix中的文件大小的单位的书写约定： 

	```
	* Applications must use IEC standard for base-2 units:
		* 1 KiB = 1,024 bytes (Note: big k)
		* 1 MiB = 1,024 KiB = 1,048,576 bytes
		* 1 GiB = 1,024 MiB = 1,048,576 KiB = 1,073,741,824 bytes
		* 1 TiB = 1,024 GiB = 1,048,576 MiB = 1,073,741,824 KiB = 1,099,511,627,776 bytes
	* Applications must use SI standard for base-10 units:
		* 1 kB = 1,000 bytes (Note: small k)
		* 1 MB = 1,000 kB = 1,000,000 bytes
		* 1 GB = 1,000 MB = 1,000,000 kB = 1,000,000,000 bytes
		* 1 TB = 1,000 GB = 1,000,000 MB = 1,000,000,000 kB = 1,000,000,000,000 bytes
	* It is not allowed to use the SI standard for base-2 units:
		* 1 kB != 1,024 bytes
		* KB (with a big k) does not exist
	```
	源：<https://wiki.ubuntu.com/UnitsPolicy>

2. 关于man文档的whatis数据库的更新:

	```
	The keywords database can become out of date. If you add additional man pages to your system, you may need to rebuild this file with mandb (Ubuntu, SUSE), makewhatis (Red Hat), or catman -w (Solaris, HP-UX, AIX).
	```
	
##Chapter 2
>这一章是关于script编程，包括bash, perl, python, ruby等。 略去不看。