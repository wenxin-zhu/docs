# GIT的基本操作-Gitee+vscode-总结


# 一、Tips：名词+本文用到的[git命令](https://so.csdn.net/so/search?q=git%E5%91%BD%E4%BB%A4&spm=1001.2101.3001.7020)

1）**SSH**：使**本地仓库**和**云端仓库**交换代码不需要每次都输入密码。（HTTP每次提交都需要）

2）.**git** ：文件夹里有这个才证明你的这个文件夹是通过git管理的。

3）**git !== gitee：**git是管理代码的命令，gitee/github是git命令的表现形式

4）查看远程仓库名字和地址：**git remote -v**

5）查看分支信息：**git branch**

**6）[其他git命令看这个](https://liaoxuefeng.gitee.io/resource.liaoxuefeng.com/git/git-cheat-sheet.html# "其他git命令看这个")**

7）放一张爽图

![](https://img-blog.csdnimg.cn/2b67334cd30a416bac867df6fc040244.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

 图0：git的各个地方

# 二、用Gitee管理代码的整体思路

## 第一步：云端配置SSH

把新电脑生成的SSH公钥放在gitee的设置里边的SSH设置上，可以参考gitee的官方文档，很nice

[生成/添加SSH公钥 - Gitee.com](https://gitee.com/help/articles/4181 "生成/添加SSH公钥 - Gitee.com")

![](https://img-blog.csdnimg.cn/594ee72dfb42414c92f627638af9df51.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

 图1：SSH公钥放的地方 

## 第二步：本地连接云端

### 第一种情况：直接从gitee上复制ssh链接，在本地vscode克隆

1）复制gitee仓库的ssh链接

![](https://img-blog.csdnimg.cn/f9e6d541c81c4615a37179bee4418259.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

 图2：复制gitee的ssh链接 

2）vscode克隆这个链接

![](https://img-blog.csdnimg.cn/32d84a5bb61748d18631f01d3a6c5350.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

图3：vscode克隆云端仓库 

连接好之后可以通过 git remote -v 查看

### 第二种情况：本地新建的文件夹同步到云端仓库

1）初始化仓库：先让这个文件夹通过git管理。

![](https://img-blog.csdnimg.cn/02997cc9cb15422dbeb5a11d386266cc.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

图4：初始化本地仓库 

2）连接云端仓库

![](https://img-blog.csdnimg.cn/4096d76140a043f0a270043813b6220f.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

图5：vscode连接远程仓库 

## 第三步：提交你的第一次代码

1）接着在本地仓库改点东西

![](https://img-blog.csdnimg.cn/a0fe2fd575bc480ba0d6778575dcaebd.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

图6：更改点本地代码 

 2）保存一下，提交到云端

![](https://img-blog.csdnimg.cn/b4db8dd527d149c995d64272e1a8d94d.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

图7：提交到云端 

 3）检查看一下云端有没有

![](https://img-blog.csdnimg.cn/867afda6ac424ce9b1ea324d24ca56bc.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA5bCR5piKfg==,size_20,color_FFFFFF,t_70,g_se,x_16)

 图8：检查看下云端有咩有

#  三、了解更多

[Git教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600 "Git教程 - 廖雪峰的官方网站")