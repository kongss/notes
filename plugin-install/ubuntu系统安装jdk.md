### ubuntu系统安装jdk
wget获取压缩文件，不可以直接解压，需要重命名 后缀名有问题
```
wget --no-check-certificate --no-cookies --header "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.tar.gz
```
进入jdk源码包所在目录,解压压缩包，命令行：
```
sudo tar xvf jdk-8u25-linux-x64.tar.gz
```
将解压后的jdk文件复制到 usr/java目录
```
sudo mv /home/plugin/jdk1.8.0_131/ /usr/java/
```
配置环境变量:vim命令打开/etc/profile文件
```
vim /etc/profile
```
在文件末尾插入如下内容
```
export JAVA_HOME=/usr/java/jdk1.8.0_131
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=$JAVA_HOME/lib:.:$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar
```
使修改生效
```
source /etc/profile 
```
查看PATH值
```
echo $PATH
```
验证是否安装成功
```
java
javac
```





