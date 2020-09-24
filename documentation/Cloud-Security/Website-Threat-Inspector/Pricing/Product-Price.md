# 产品价格

网站威胁扫描产品分为**基础版**和**付费版**两类，付费版包含**包年包月（企业版）**和**按量付费**两大版本。

付费版本的具体价格折扣，详见：https://threatscanner-console.jdcloud.com/jsecscanner/create?version=basic

您可根据您的域名资产数量选择合适的服务版本进行使用。

## 产品版本定义

| 产品版本           | 版本定义                                                     |
| :----------------- | :----------------------------------------------------------- |
| 基础版             | 产品开通后，属于基础版未付费状态，拥有5次免费扫描额度，开通服务后1年内有效。每扫描一次子域名或IP，扣减一次额度，直至次数用尽后，回归基础版查看；基础版支持针对容器镜像文件的威胁风险进行免费扫描（10个镜像/天） |
| 按次付费版         | 按次计费形式，按次进行服务购买，每扫描一次子域名或IP，扣减一次额度，直至次数用尽 |
| 包年包月（企业版） | 每购买1个单位的**实例包**，提供1个一级域名（例如：[jd.com](http://jd.com/)），不限制该域名对应的子域名和IP数量。在企业版中，支持购买扩展实例包，每个单位的**扩展实例包**，提供1个一级域名（例如：[jd.com](http://jd.com/)），限制对应子域名或者IP数量小于10个） |

## 产品版本规格

| 版本规格        | 包年包月（企业版） | 按量付费版 | 基础版 |
| --------------- | ------------------ | ---------- | ------ |
| web漏洞检测     | 支持               | 支持       | 支持查看历史扫描记录   |
| 弱密码检测      | 支持               | 支持       | 支持查看历史扫描记录   |
| 端口风险检测    | 支持               | 支持       | 支持查看历史扫描记录   |
| API风险检测    | 支持               | 支持       | 支持查看历史扫描记录   |
| 资产关联发现    | 支持               | 支持       | 支持查看历史扫描记录   |
| 容器镜像风险检测    | 支持（100个镜像/天）    | 支持（100个镜像/天）       | 支持（10个镜像/天）   |
| 扫描场景：互联网资产  | 支持               | 支持       | 支持查看历史扫描记录   |
| 扫描场景：VPC内网资产 | 支持<br>针对扫描的vpc子网，需单独支付扫描探针（容器实例）的费用 | 支持<br>针对扫描的vpc子网，需单独支付扫描探针（容器实例）的费用 | 不支持 |
| 扫描场景：外部IDC资产 | 支持<br/>需要在IDC环境手动部署本地扫描探针 | 支持<br/>需要在IDC环境手动部署本地扫描探针 | 不支持 |
| 购买扩展实例包  | 支持               | 不支持     | 不支持 |

#### VPC内网扫描探针费用说明

针对租户内VPC内网扫描，需要在每个VPC子网中部署扫描探针（以容器实例为载体），需要单独支付相关费用。

具体以最新容器实例按配置计费的价格为准，https://cns-console.jdcloud.com/host/container/create?dataCenter=cn-north-1