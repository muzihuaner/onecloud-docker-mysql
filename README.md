# onecloud-docker-mysql
玩客云-docker部署mysql和phpadmin

首先安装docker

安装Docker
```
curl -sSL https://get.docker.com/ | sh 
systemctl start docker 
systemctl enable docker
``` 

2、安装Docker Compose
```
apt-get install docker-compose -y
curl -L "https://github.com/docker/compose/releases/download/1.25.3/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
``` 

你也可以为Docker Compose创建一个快捷键，创建好以后，就可以直接用dc命令替代docker compose了。
```
chmod a+x /usr/local/bin/docker-compose
rm -rf `which dc`
ln -s /usr/local/bin/docker-compose /usr/bin/dc
``` 

 

二、Mysql+PHPMyAdmin的部署
1、创建文件夹
```
mkdir db && cd db
 
```
2、创建docker-compose.yml文件
```
nano docker-compose.yml
 ```

写入
 

3、启动
```
docker-compose up -d
 ```

至此，Mysql+PHPMyAdmin就装完了，有了PHPMyAdmin，也就容易操作Mysql了。

