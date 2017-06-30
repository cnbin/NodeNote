	参考网站：
	http://www.runoob.com/mongodb/mongodb-linux-install.html
	http://blog.csdn.net/playstudy/article/details/50149021
	
###1.到Mongodb官网下载

![img](http://wx3.sinaimg.cn/mw690/78f9859egy1fh3d0kdlyrj20j80fdmyq.jpg)
###2.进入到压缩包所在目录，执行

	tar -zxvf mongodb-osx-x86_64-3.4.5.tgz
	mv  mongodb-osx-x86_64-3.4.5/ /usr/local/mongodb  # 将解压包拷贝到指定目录

###MongoDB 的可执行文件位于 bin 目录下，所以可以将其添加到 PATH 路径中：

	export PATH=<mongodb-install-directory>/bin:$PATH
	<mongodb-install-directory> 为你 MongoDB 的安装路径。如这里的 /usr/local/mongodb 。

![img](http://wx3.sinaimg.cn/mw690/78f9859egy1fh3d0nsb61j20fr07wmxk.jpg)
	
###创建数据库目录
MongoDB的数据存储在data目录的db目录下，但是这个目录在安装过程不会自动创建，所以你需要手动创建data目录，并在data目录中创建db目录。
以下实例中我们将data目录创建于根目录下(/)。
注意：`/data/db` 是 MongoDB 默认的启动的数据库路径(--dbpath)。

	mkdir -p /data/db
	
###注意：data目录需要修改权限，改为读与写。否则无法运行。

![img](http://wx3.sinaimg.cn/mw690/78f9859egy1fh3d0r2e68j20aw0gn3zz.jpg)

###终端运行：./mongod，显示如下图内容泽代表成功启动

![img](http://wx1.sinaimg.cn/mw690/78f9859egy1fh3d0tvwo0j20ts09xn0v.jpg)

###关闭Mongodb:直接用ctrl+c

###进入Mongodb后台，新开一个终端窗口，切记，前提是./mongod运行成功了。操作步骤：进入/usr/local/mongodb/bin目录，执行./mongo，如下图显示则代表成功进入管理后台。

![img](http://wx2.sinaimg.cn/mw690/78f9859egy1fh3d0xh8asj20fo09sjsx.jpg)
