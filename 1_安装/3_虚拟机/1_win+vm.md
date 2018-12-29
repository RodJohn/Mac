

# 1 概述

概述

	在windows下使用VMware（14）虚拟mac（OS X 10.14）
	在使用中不会有明显的的卡顿（使用如下配置）



# 2 准备

## 硬件

	win10（固态硬盘+12G内存）
	Mac （分配4core/8g）
		
## 软件

	https://www.sysceo.com/forum/thread-43341-1-1.html


# 3 安装vmware

	windows安装vmware教程
	(https://blog.csdn.net/rod_john/article/details/83755783)

# 4 安装Unlocker

原理

	VMware本身不支持Mac OS X的安装，
	添加这个补丁才能支持Mac OS X的安装。

	
使用
	
	将Unlocker解压，右击win-install.cmd，选择“以管理员身份运行”

安装报错

	执行Unlocker时报错 “gettools.exe 已停止工作”
	执行文件夹中的 win-update-tools.cmd 文件
	方案来自（https://blog.csdn.net/testcs_dn/article/details/78697643）
		

# 5 新建Mac虚拟

1.新建
	
	新建虚拟机
	选择典型安装
	

2.选择镜像安装

	选择前面下载的镜像文件（CDR和ISO都可以）
	
3.选择系统

	选择Apple Mac，版本可以选高一点
	如果这里找不到Apple Mac，就说明前面的Unlocker插件没安装好

![](../../../pic/虚拟安装黑苹果/vm选项.png)

4.选择安装名称和位置

	记住这个安装位置
	虚拟机文件就在这里
	
5.配置硬盘
	
	硬盘使用固态
	分配60G同时把文件存为单个文件


6.配置虚拟机资源

    选择虚拟机配置
	cpu设置4core
	内存设置8g
	

# 6 安装Mac


## 启动安装

    启动刚刚创建的虚拟机
    如果出现下图，则表示进入Mac安装过程
	
![](../../../pic/虚拟安装黑苹果/正常安装.png)


### 启动报错

问题

![](../../../pic/虚拟安装黑苹果/安装报错.png)
    
    
解决方案

	编辑VMX文件（在前面选择虚拟mac的位置），
	在 smc.present = "TRUE" 后面添加了 smc.version = 0
    参考文章（https://blog.csdn.net/testcs_dn/article/details/51343988）


![](../../../pic/虚拟安装黑苹果/报错处理.png)	


		
## 	正常安装

	到此为止进入正常安装mac
	接下来参考（https://blog.csdn.net/rod_john/article/details/83756178）


	
# 7 优化

## vmware常用优化

	vmtools、共享文件夹
	(https://blog.csdn.net/rod_john/article/details/83659020)


# 参考

https://blog.csdn.net/u011415782/article/details/78505422
https://www.jianshu.com/p/db787997057f


