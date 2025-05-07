## 1.拉取镜像
```shell
docker pull apache/rocketmq:5.3.2
```
## 2.创建容器共享网络
```shell
docker network create my-network
```
## 3.配置Broker的IP地址
默认注册的是当前主机的IP
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
### 使用Admin Tool
#### 查看集群信息
broker注册的IP必须是互相联通的
```shell
cd /home/rocketmq/rocketmq-5.3.2/bin
sh mqadmin clusterList -n rmqnamesrv:9876
```
官网地址：https://rocketmq.apache.org/zh/docs/quickStart