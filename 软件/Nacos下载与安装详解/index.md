## Nacos下载与安装详解

#### 一、安装与下载

下载地址：https://github.com/alibaba/nacos/releases



我这里下载的windows版本的，不需要安装，下载好直接解压，然后到bin目录下，执行startup.cmd -m standalone启动即可

命令运行成功后直接访问http://localhost:8848/nacos
默认账号密码都是nacos

nacos默认为cluster集群模式启动，在启动文件startup.cmd中修改保存配置为standalone单例模式启动就可以了，这样启动的时候直接执行startup.cmd就可以了，不需要再使用startup.cmd -m standalone命令启动了！


#### 二、数据持久化

Nacos默认自带的是嵌入式数据库derby

Apache Derby是一个完全用java编写的数据库，Derby是一个Open source的产品，基于Apache License 2.0分发。Apache Derby非常小巧，核心部分derby.jar只有2M，所以既可以做为单独的数据库服务器使用，也可以内嵌在应用程序中使用。

nacos源码：https://github.com/alibaba/nacos/blob/develop/config/pom.xml

假如做数据迁移等等，有时候我们更希望将数据保存到mysql当中，而不是内嵌数据库当中，Nacos也提供了mysql数据持久化的方式。

数据库sql脚本：https://github.com/alibaba/nacos/blob/master/config/src/main/resources/META-INF/nacos-db.sql

##### 1.新建一个数据库，然后执行脚本

执行的时候遇到问题，报错1071 - Specified key was too long; max key length is 767 bytes，我使用的mysql版本有点低，用的是5.5.25a-log版本，高版本应该不会报错。

解决办法：https://blog.csdn.net/weixin_43888891/article/details/121542530

