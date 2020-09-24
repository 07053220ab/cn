# 核心概念

### 1.日志主题 

日志主题是日志采集存储的单位，方便用户将某应用程序所产生的同类型的日志进行统一存储。 

### 2.日志集

日志集是日志主题管理的单位，用于保存某服务下不同应用程序产生的各类日志主题。  

**举例说明**

用户有一个服务A，需要用到两个应用，APP1和APP2，APP1部署在VM1和VM2上，APP2部署在VM3和VM4上，APP1会产生两类日志LogA和LogB，APP2会产生两类日志Log1和Log2。

用户可创建服务A日志集，并在该日志集下分别创建日志主题Topic_1、Topic_2、Topic_3、Topic_4，分别用于采集LogA、LogB、Log1、Log2四种不同类型的日志。从而对对特定类型的日志设置转储和监控。

![](https://raw.githubusercontent.com/jdcloudcom/cn/zhangwenjie-only/image/LogService/Introduction/logset%26logtopic.jpg)

### 3.日志源设置

日志源设置是指采集日志相关的配置信息，需指定日志来源，支持云产品日志和用户的业务应用日志作为日志源。

云产品日志源是指日志的来源为云产品。用户在控制台购买云产品后，云产品默认可提供给用户查看的日志。云产品日志无需用户定义字段和格式，无需用户安装日志采集agent，由京东智联云后端上报或采集。用户只需创建对应的云产品日志类型的日志配置即可。

业务应用日志是指用户在京东智联云上部署的业务应用所产生的日志。日志内容和日志格式由用户自己定义。用户无需手动安装日志采集agent，只需要在日志源设置中选择需要采集的云主机，日志采集agent将会自动安装。支持单行和多行的业务应用日志作为日志源。业务应用日志支持投递至多种类型的目的地，默认采集至日志服务的日志主题中。也可将日志投递至控制台的云ES和云Kafka中，或自建ES和自建Kafka中。

### 4.全文检索

全文检索，即关键词检索。日志中的内容不区分key和value，只要符合检索条件即可。如想搜索包含“error”的日志，只需在搜索框中输入“error”即可。特殊字符如“-”、“/”等作为分词符无法搜索。请在检索条件中避免出现特殊字符。

### 5.键值检索 

键值检索，即对日志内容的键值对进行检索。日志中的内容区分key和value，可以针对特定Key的值进行快速精确的查询。如想搜索状态码大于300的，可在快捷检索中选择状态码的KEY，如statusCode，operator选择“>”，VALUE输入300，点击“检索”按钮即可搜索出符合条件的日志；也可在高级检索中输入**statusCode > 300**,点击“检索”按钮即可搜索出符合条件的日志。

### 6.日志转储

日志服务计费后，将会对用户存储在日志服务中的日志数据进行收费，长期存储在日志服务中会增加用户的存储成本；此外，对于部分用户而言，日志服务提供的日志分析功能可能无法满足需求，所以有离线分析的需求。因此，日志服务支持用户将日志数据转储至对象存储OSS中，支持多种格式和压缩转储，以此降低用户的成本。将日志数据按照设置的转储规则存储对对象存储OSS中，并且可以在所转储的对象存储bucket中下载日志文件，进行审计、离线分析等。

### 7.日志监控

在企业的运维中，最不愿看到的就是当业务出现问题时，没有及时发现；以及不能实时掌握业务的运营情况。因此，为了便于用户及时地了解业务运营情况，以及快速的发现问题，降低损失，日志服务提供日志监控的功能。用户可以针对有监控需求的日志，设置筛选条件，对符合筛选条件的日志数据中的关键词或指定字段设置监控，可以查看监控图，设置报警规则。