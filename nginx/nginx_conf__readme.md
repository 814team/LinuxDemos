����/ԭ��

centos7

vm10

����/����

�鿴�Ƿ��Ѿ���װ��REPC

rpm -qa | grep ��REPC��

�õ� ���￴���Ѿ���װ�ˡ�

ͬ�� �鿴openssl ?gzip ?wget

���û�а�װ��ʹ��yum���װ�£���Ҫ��rootȨ���²���

�ֱ���

yum install pcre*
yum install?openssl*
yum install zlib?
yum install zlib-devel
yum install wget
 ���￴�� ���ĸ����� ����װ����


���濪ʼ��װnginx
.
�Ȼ�ȡ��wget http://nginx.org/download/nginx-1.8.0.tar.gz
.

����İ汾�ſ��Ը��ĵģ����������������½http://nginx.org/download/ ?Ȼ������Ҫ����ʲô�汾��Ŀǰ�ߵ����в��԰� �ȶ��� �ɰ� ����?
.
PS���㵱ǰλ�����ģ����ص��ļ�������
.

���غ����Ժ��Լ��Ҹ�λ�ø��ƹ�ȥ,Ȼ���ѹ���������Ƿ�����/usr/local
.
cp?nginx-1.8.0.tar.gz /usr/local
.
cd /usr/local
.
tar -zxvf nginx-1.8.0.tar.gz
.
.
��ѹ��ϣ���ȥ����װ��
.
cd?nginx-1.8.0
.
./configure --prefix=/usr/local/nginx-1.8.0 \--with-http_ssl_module --with-http_spdy_module \--with-http_stub_status_module --with-pcre
.
.
ִ���������
.
make && make install?
.
.
֮����밲װĿ¼?
.
Ȼ�� ���� ./sbin/nginx
.
ps -ef|grep "nginx"
.
�鿴�����Ƿ����� ����������

.
���� ��װ����ˡ�
.
�޸�conf/nginx.conf ?��������� ֮�� ����nginx ����
.
./sbin/nginx -s reload
