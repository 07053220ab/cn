## IP黑白名单配置

在WAF中，您可以配置精准访问控制规则来阻断或放行指定IP的访问请求，即设置IP黑/白名单。IP黑白名单仅针对配置的特定域名生效。

### **操作步骤**

参照以下步骤，配置IP黑名单和IP白名单：

**说明：** 执行以下操作前，请确保已将网站接入WAF进行防护。具体操作请参考[CNAME接入指南](file:///E:\WMM\%E5%B7%A5%E4%BD%9C%E6%80%BB%E7%BB%93\WAF%E6%96%87%E6%A1%A3\%E4%BA%91WAF\Introduction\%E9%98%B2%E6%8A%A4%E9%85%8D%E7%BD%AE\cn.zh-CN\%E7%94%A8%E6%88%B7%E6%8C%87%E5%8D%97\%E6%8E%A5%E5%85%A5WAF\CNAME%E6%8E%A5%E5%85%A5%E6%8C%87%E5%8D%97.md)。

1. 登录[京东云Web应用防火墙控制台](https://yundun.console.aliyun.com/?p=waf)。

2. 前往**网站配置**页面。

3. 选择要操作的域名，单击其操作列下的**防护配置**。

4. 在**精确访问控制**下，开启防护，并单击**前去配置**。![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\msohtmlclip1\01\clip_image002.png)

5. 单击**新增规则**，新增一条防护规则。

6. - 白名单配置示例：使用下图配置，放行源IP为1.1.1.1的所有访问。

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png)

**说明：** 如果想完全放行这个IP的所有请求，则不要勾选**匹配动作**下方的继续执行其它防护选项。如果勾选，则来自此IP的请求会继续通过相应的规则校验。

1. - 黑名单配置示例：使用下图配置，阻断源IP为1.1.1.1的所有访问。

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\msohtmlclip1\01\clip_image006.png)

**注意事项**

- 多条防护规则之间存在匹配优先级，按照规则列表中从上到下的顺序进行匹配，通过单击右上角的**规则排序**可以调整防护规则之间的优先级。

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\msohtmlclip1\01\clip_image008.png)

**相关参考**

- [产品简介](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Advanced-Anti-DDoS/Introduction/What-Is-Advanced-Anti-DDoS.md)
- [产品定价](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Advanced-Anti-DDoS/Pricing/Billing-Rules.md)
- [常见问题](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Advanced-Anti-DDoS/Pricing/Billing-Rules.md)

 