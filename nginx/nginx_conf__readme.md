工具/原料

centos7

vm10

方法/步骤

查看是否已经安装了REPC

rpm -qa | grep “REPC”

好的 这里看到已经安装了。

同理 查看openssl ?gzip ?wget

如果没有安装则使用yum命令安装下，需要在root权限下操作

分别是

yum install pcre*
yum install?openssl*
yum install zlib?
yum install zlib-devel
yum install wget
 这里看到 这四个东西 都安装好了


下面开始安装nginx
.
先获取包wget http://nginx.org/download/nginx-1.8.0.tar.gz
.

后面的版本号可以更改的，可以先用浏览器登陆http://nginx.org/download/ ?然后看下你要的是什么版本，目前高到底有测试版 稳定版 旧版 三种?
.
PS：你当前位置在哪，下载的文件就在哪
.

下载好了以后，自己找个位置复制过去,然后解压。我这里是放在了/usr/local
.
cp?nginx-1.8.0.tar.gz /usr/local
.
cd /usr/local
.
tar -zxvf nginx-1.8.0.tar.gz
.
.
解压完毕，进去，安装。
.
cd?nginx-1.8.0
.
./configure --prefix=/usr/local/nginx-1.8.0 \--with-http_ssl_module --with-http_spdy_module \--with-http_stub_status_module --with-pcre
.
.
执行这个命令
.
make && make install?
.
.
之后进入安装目录?
.
然后 启动 ./sbin/nginx
.
ps -ef|grep "nginx"
.
查看服务是否启动 有两个服务

.
至此 安装完毕了。
.
修改conf/nginx.conf ?来完成配置 之后 重启nginx 服务
.
./sbin/nginx -s reload
