# 产品概述

日志服务（Log Service）是京东智联云提供的一站式日志服务平台。提供日志实时采集与存储，日志的查询检索，日志实时投递消费，日志实时监控等功能，协助用户通过日志解决业务运营，业务监控，问题定位等需求。

# 产品功能架构

![功能架构图](https://raw.githubusercontent.com/jdcloudcom/cn/zhangwenjie-only/image/LogService/Introduction/structure.jpg)

# 产品功能简介
## 日志采集
1. 云产品日志自动采集。
2. 业务应用日志自动安装日志采集agent，无需手动安装。
3. 业务应用日志支持直接从agent端采集至云ES、自建ES、云Kafka、自建Kafka。
4. 业务应用日志支持选择实例、高可用组、标签，满足大中小型客户的需求。
5. 支持多行日志的采集。
6. 业务应用日志支持对日志内容的格式化提取。

## 日志检索
1. 支持键值、关键词、meta内容的检索。
2. 支持查询上下文。
3. 根据不同业务人员的特点，键值检索支持快捷检索和高级检索。

## 日志转储
1. 支持用户将云产品日志转储至对象存储OSS中。
2. 支持对转储的日志内容进行压缩，snappy格式和gzip格式。
3. 支持原文转储和JSON格式的转储。

## 日志监控
1. 支持对关键词设置监控指标
2. 支持对键值设置监控指标
3. 支持跳转至云监控中的自定义监控设置报警规则