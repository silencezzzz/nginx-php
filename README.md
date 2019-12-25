<center size=100>*nginx-php*</center>

> 寂寞，成为更好的自己

### 主要特性

基于**Alpine Linux**最小化Linux环境加速构建镜像。

安装了nginx 1.17.5，php 7.3.4。PHP的拓展支持redis，mongodb，memcache，grpc，protobuf，swoole，yaf，mysql，mbstring，bmath，curl，mhash  
不需要啥就注释啥

*注:阿里郎的网络真心对php、nginx官网不友好  经常下载丢包然后退出  因此带了本地文件  不放心的小朋友将dockerfile对应行注释换上官网链接即可~*


***

### 直接拉取镜像使用  则不需要往后步骤
```
docker pull joker950618/nginx-php:v1
```

### 构建镜像
``` 
git clone https://github.com/silencezzzz/nginx-php.git

docker build --no-cache -t nginx-php:v1 .
```
### 启动镜像
```
docker run -d -p 8080:80 --name=nginx-php nginx-php:v1
```
### 进入镜像容器内
```
docker exec -it nginx-php sh
```
### 推送镜像
```
docker login # 先登录

docker tag nginx-php:v1 yourName/nginx-php:v1

docker push yourName/nginx-php:v1
```
### 效果
![Image text](https://raw.githubusercontent.com/silencezzzz/img/master/php7.3.4-nginx.jpg)
![Image text](https://raw.githubusercontent.com/silencezzzz/img/master/phpkuozhan.jpg)




