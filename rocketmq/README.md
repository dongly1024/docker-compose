## 1.拉取镜像
```shell
docker pull apache/rocketmq:5.3.2
```
## 2.创建容器共享网络
```shell
docker network create my-network
```
## 3.配置Broker的IP地址
### Linux
```shell
echo "brokerIP1=127.0.0.1" > broker.conf
```
### Windows
```shell
echo "brokerIP1=127.0.0.1" > broker.conf
```
## 4.启动RocketMQ
### Linux
```shell
docker-compose up -d
```
### Windows
```shell
docker-compose -p rockermq_project up -d
```
官网地址：https://rocketmq.apache.org/zh/docs/quickStart