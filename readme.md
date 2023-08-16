# NOAH

## BIGTOP

* docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:bigtop-repo-ready-for-http
* docker run -itd --name='bigtop320' --privileged -p 2929:2929 registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:bigtop-repo-ready-for-http /usr/sbin/init

## Ambari

### 备份

* docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:20230803-bak
* docker run -itd --name='ambari' --hostname='ambari-server' registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:20230803-bak

### RAW

* docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ready-for-ambari-install
* docker run -itd --name='noah' -p 8000:8000 -p 8080:8080 -p 50070:50070 -p 8088:8088 -p 19888:19888 -p 3000:3000 -p 10002:10002 -p 16010:16010 -p 18081:18081 -p 9995:9995 -p 8082:8082 -p 8983:8983 -p 8440:8440 -p 8441:8441 -p 9092:9092 -p 4040:4040 -p 4041:4041 -p 9000:9000 -p 10086:10086 -p 5432:5432 -p 8081:8081 -p 18030:18030 -p 19020:19020 -p 19030:19030 -p 19010:19010 -p 19050:19050 -p 19060:19060 -p 18040:18040 -p 18060:18060 -p 18088:18088 --hostname='noah' --privileged registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ready-for-ambari-install

### INSTALLED

* docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ambari-installed
* docker run -itd --name='noah' -p 8000:8000 -p 8080:8080 -p 50070:50070 -p 8088:8088 -p 19888:19888 -p 3000:3000 -p 10002:10002 -p 16010:16010 -p 18081:18081 -p 9995:9995 -p 8082:8082 -p 8983:8983 -p 8440:8440 -p 8441:8441 -p 9092:9092 -p 4040:4040 -p 4041:4041 -p 9000:9000 -p 10086:10086 -p 5432:5432 -p 8081:8081 -p 18030:18030 -p 19020:19020 -p 19030:19030 -p 19010:19010 -p 19050:19050 -p 19060:19060 -p 18040:18040 -p 18060:18060 -p 18088:18088 --hostname='noah' --privileged registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ambari-installed

## Streampark

* docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:install-streampark-dev
* docker run -itd --name='noah' -p 8000:8000 -p 8080:8080 -p 50070:50070 -p 8088:8088 -p 19888:19888 -p 3000:3000 -p 10002:10002 -p 16010:16010 -p 18081:18081 -p 9995:9995 -p 8082:8082 -p 8983:8983 -p 8440:8440 -p 8441:8441 -p 9092:9092 -p 4040:4040 -p 4041:4041 -p 9000:9000 -p 10086:10086 -p 5432:5432 -p 8081:8081 -p 18030:18030 -p 19020:19020 -p 19030:19030 -p 19010:19010 -p 19050:19050 -p 19060:19060 -p 18040:18040 -p 18060:18060 -p 18088:18088 --hostname='noah' --privileged registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:install-streampark-dev

## Doris + Spiderflow

* docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ready-for-sql-dev-20230812
* docker run -itd --name='noah' -p 8000:8000 -p 8080:8080 -p 50070:50070 -p 8088:8088 -p 19888:19888 -p 3000:3000 -p 10002:10002 -p 16010:16010 -p 18081:18081 -p 9995:9995 -p 8082:8082 -p 8983:8983 -p 8440:8440 -p 8441:8441 -p 9092:9092 -p 4040:4040 -p 4041:4041 -p 9000:9000 -p 10086:10086 -p 5432:5432 -p 8081:8081 -p 18030:18030 -p 19020:19020 -p 19030:19030 -p 19010:19010 -p 19050:19050 -p 19060:19060 -p 18040:18040 -p 18060:18060 -p 18088:18088 --hostname='noah' --privileged registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ready-for-sql-dev-20230812

## EFAK

* docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ready-for-sql-dev-20230815
* docker run -itd --name='noah' -p 8000:8000 -p 8080:8080 -p 50070:50070 -p 8088:8088 -p 19888:19888 -p 3000:3000 -p 10002:10002 -p 16010:16010 -p 18081:18081 -p 9995:9995 -p 8082:8082 -p 8983:8983 -p 8440:8440 -p 8441:8441 -p 9092:9092 -p 4040:4040 -p 4041:4041 -p 9000:9000 -p 10086:10086 -p 5432:5432 -p 8081:8081 -p 18030:18030 -p 19020:19020 -p 19030:19030 -p 19010:19010 -p 19050:19050 -p 19060:19060 -p 18040:18040 -p 18060:18060 -p 18088:18088 -p 2181:2181 -p 18048:18048 -p 18085:18085  --hostname='noah' --privileged registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ready-for-sql-dev-20230815

## Flink 任务调试

* docker pull registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ready-for-sql-dev-20230816
* docker run -itd --name='noah' -p 8000:8000 -p 8080:8080 -p 50070:50070 -p 8088:8088 -p 19888:19888 -p 3000:3000 -p 10002:10002 -p 16010:16010 -p 18081:18081 -p 9995:9995 -p 8082:8082 -p 8983:8983 -p 8440:8440 -p 8441:8441 -p 9092:9092 -p 4040:4040 -p 4041:4041 -p 9000:9000 -p 10086:10086 -p 5432:5432 -p 8081:8081 -p 18030:18030 -p 19020:19020 -p 19030:19030 -p 19010:19010 -p 19050:19050 -p 19060:19060 -p 18040:18040 -p 18060:18060 -p 18088:18088 -p 2181:2181 -p 18048:18048 -p 18085:18085  --hostname='noah' --privileged registry.cn-hangzhou.aliyuncs.com/wujundi/centos-noah:ready-for-sql-dev-20230816

## RANDOM API

* https://randomuser.me/api/
