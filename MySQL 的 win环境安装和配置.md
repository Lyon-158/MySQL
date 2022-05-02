## 

# MySQL 的 win环境安装和配置

## 具体步骤

### 第一步：去官网下载、安装，网址如下

https://dev.mysql.com/get/Downloads/MySQL-8.0/mysql-8.0.29-winx64.ziphttps://dev.mysql.com/get/Downloads/MySQL-8.0/mysql-8.0.29-winx64.zip

建议使用迅雷下载，浏览器太慢

### 【第二步】：先解压到目录 D:/mysql 下，（保证bin的路径为  D:/mysql/bin）<mark>注意：版本 8.0.19 后不用配置my.ini</mark>

### 第三步：在系统环境变量 path里加上 mysql路径

``` 
D:\mysql\bin    //我的bin在此路径下
```

### 【第四步】：打开cmd（管理员），输入下方语句

```cmd
mysqld --initialize-insecure --user=mysql    //耐心等待
```

### 完成后，输入

```
mysqld -install    //出现 Service successfully installed. 就配置完成了！
```

>  到这里，其实<mark>已经配置完成了</mark> ，下面的步骤是<mark>如何启动 MySQL</mark> 

 

# 如何启动MySQL

### 第一步：运行cmd（管理员）<mark>切记：一定要管理员</mark>

### 第二步：启动MySQL数据库

```
 net start mysql    //MySQL 服务已经启动成功
```

## 第三步：进入数据库，//-u是用户名，-p是密码；由于没有创建密码，看到Enter password后，直接回车即可

```
mysql -u root -p    //回车后输入密码
```



![](C:\Users\admin\AppData\Roaming\marktext\images\2022-05-02-11-34-40-image.png)



### 第四步：更改MySQL密码，在mysql>下输入该命令

```
alter user user() identified by "";    //"密码内容在此"，显示OK就好了
```

![](C:\Users\admin\AppData\Roaming\marktext\images\2022-05-02-11-39-39-image.png)

<mark>注意：已修改过密码，使用第一步的命令登录，登录数据库时的密码使用当前密码</mark> 

> 至此，MySQL的安装、配置和开启服务登录使用的过程就结束了，可以开启你的MySQL学习之旅了。
