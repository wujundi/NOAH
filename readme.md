# PROJECT NOAH

项目名称灵感来自于诺亚方舟，该项目旨在未数据开发人员提供一个简单的，紧跟技术发展趋势的一站式学习与测试环境

## 一、能从项目中获得什么环境？

### 1、ambari 2.8.0 的全部组件，包含（对应 bigtop 3.2.0 的组件栈）：

| Service        | Version  | Description                                                                                                                                                                   |
| -------------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| HDFS           | 3.3.4-1  | Apache Hadoop Distributed File System                                                                                                                                         |
| YARN           | 3.3.4-1  | Apache Hadoop NextGen MapReduce (YARN)                                                                                                                                        |
| MapReduce2     | 3.3.4-1  | Apache Hadoop NextGen MapReduce (YARN)                                                                                                                                        |
| Tez            | 0.10.1-1 | Tez is the next generation Hadoop Query Processing framework written on top of YARN.                                                                                          |
| Hive           | 3.1.3-1  | Data warehouse system for ad-hoc queries & analysis of large datasets and table & storage management service                                                                  |
| HBase          | 2.4.13-1 | Non-relational distributed database and centralized service for configuration management & synchronization                                                                    |
| ZooKeeper      | 3.5.9-2  | Centralized service which provides highly reliable distributed coordination                                                                                                   |
| Ambari Metrics | 3.0.0    | A system for metrics collection that provides storage and retrieval capability for metrics collected from the cluster                                                         |
| Kafka          | 2.8.1-2  | A high-throughput distributed messaging system                                                                                                                                |
| Spark          | 3.2.3-1  | Apache Spark is a unified analytics engine for large-scale data processing.                                                                                                   |
| Zeppelin       | 0.10.1-1 | A web-based notebook that enables interactive data analytics. It enables you to make beautiful data-driven, interactive and collaborative documents with SQL, Scala and more. |
| Flink          | 1.15.3-1 | Flink is a framework and distributed processing engine for stateful computations over unbounded and bounded data streams                                                      |
| Solr           | 8.11.2-1 | Solr is the popular, blazing-fast, open source enterprise search platform built on Apache Lucene.                                                                             |

### 2、流任务管理平台 streampark 2.1.1

![1699102298789](image/readme/1699102298789.png)

### 3、OLAP 引擎 doris 1.2.4.1![1699102046313](image/readme/1699102046313.png)

### 4、图形化配置式爬虫平台 spiderflow 0.5.0

![1699102157752](image/readme/1699102157752.png)

### 5、Kafka 管理平台 EFAK 3.0.1

## 二、需要什么前置条件？

你需要一个 docker 环境（建议给到充裕一些的内存容量，本人测试容器内存为48G）

## 三、如何启动？

### STEP 1 拉取镜像

docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/share:noah-milestone-1-20231031

### Step 2 运行容器

docker run -itd --name='noah' -p 8000:8000 -p 8080:8080 -p 50070:50070 -p 8088:8088 -p 19888:19888 -p 3000:3000 -p 10002:10002 -p 16010:16010 -p 18081:18081 -p 9995:9995 -p 8082:8082 -p 8983:8983 -p 8440:8440 -p 8441:8441 -p 9092:9092 -p 4040:4040 -p 4041:4041 -p 9000:9000 -p 10086:10086 -p 5432:5432 -p 8081:8081 -p 18030:18030 -p 19020:19020 -p 19030:19030 -p 19010:19010 -p 19050:19050 -p 19060:19060 -p 18040:18040 -p 18060:18060 -p 18088:18088 -p 2181:2181 -p 18048:18048 -p 18085:18085 -p 8020:8020 --hostname='noah' --privileged registry.cn-hangzhou.aliyuncs.com/wujundi/share:noah-milestone-1-20231031

### Step 3 进入容器

具体方式因人而异，这里推荐使用 vscode 的 Dev Containers 插件

### Step 4 开启后端服务

在容器中执行 bash /opt/start_up.sh

### Step 5 启动 ambari 内的各个组件

浏览器访问 http://127.0.0.1:8080/#/login，Username 输入 admin，Password 输入 admin，登录之后，在左侧 Service 后面的三个点中，点击【Start All】，等待组件各组件启动


## 附：各组件访问 url 及用户名密码
