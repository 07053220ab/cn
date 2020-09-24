# 应用场景

以下说明数据传输 DTS 的使用场景。

## 数据热迁移上云

DTS 支持不停服数据迁移，迁移过程中持续获取源数据库的增量数据并更新到目标数据库，数据迁移期间不影响源数据库对外提供服务，从而最大程度地减少上云过程对业务的影响。

![1570775871943](../../../../image/Data-Transmission-Service/dts-005.png)



## 业务异步解耦

通过DTS提供的数据订阅服务，可以将深耦合的业务优化为通过实时消息通知实现的异步耦合，如：业务系统A完成数据写入后直接返回，底层通过DTS的数据订阅实时获取数据变更，业务系统B通过SDK订阅这些变更数据。

![image-20200629182618385](../../../../image/Data-Transmission-Service/dts-036.png)


