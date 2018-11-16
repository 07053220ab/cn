## 恶意IP惩罚

恶意IP惩罚帮助您自动封禁在短时间内进行多次Web攻击的客户端IP。

### **功能描述**

传统的Web应用防火墙针对IP-URL维度进行拦截。当判定一个请求是攻击行为后，单次阻断该请求。而实际上，攻击者们可能持续不断地在对您的网站进行扫描、攻击，研究防护策略并尝试绕过防火墙，单次阻断的处理方式在这种情况下往往不够高效。

针对这种情况，京东云Web应用防火墙提供恶意IP惩罚功能。当一个IP被WAF识别到正在进行持续的攻击行为时，WAF自动封禁该恶意IP。

**操作步骤**

参照以下步骤，启用恶意IP惩罚功能：

**说明：** 执行以下操作前，请确保已将网站接入WAF进行防护。具体操作请参考[CNAME接入指南](file:///E:\WMM\%E5%B7%A5%E4%BD%9C%E6%80%BB%E7%BB%93\WAF%E6%96%87%E6%A1%A3\%E4%BA%91WAF\Introduction\%E9%98%B2%E6%8A%A4%E9%85%8D%E7%BD%AE\cn.zh-CN\%E7%94%A8%E6%88%B7%E6%8C%87%E5%8D%97\%E6%8E%A5%E5%85%A5WAF\CNAME%E6%8E%A5%E5%85%A5%E6%8C%87%E5%8D%97.md)。

1. 登录[京东云Web应用防火墙控制台](https://cloudwaf-console.jdcloud.com)。
2. 前往**网站配置**页面。
3. 选择要操作的域名，单击其操作列下的**防护配置**。
4. 在**恶意IP惩罚**下，启用防护。默认的防护规则是：当WAF在1分钟内拦截到一个IP发动的2次Web攻击时，就封禁该IP的访问请求6分钟。

**说明：** 如果使用中出现异常，可以在此页面关闭防护。

![img](file:///C:\Users\ZHANGJ~1\AppData\Local\Temp\msohtmlclip1\01\clip_image002.png)

**测试示例**

启用恶意IP惩罚后，当您的网站遭受扫描器扫描或黑客持续攻击时，WAF在很短的时间内就会识别并阻断攻击IP的所有访问行为，极大的增加黑客的攻击成本。

**相关参考**

- [产品简介](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Advanced-Anti-DDoS/Introduction/What-Is-Advanced-Anti-DDoS.md)
- [产品定价](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Advanced-Anti-DDoS/Pricing/Billing-Rules.md)
- [常见问题](https://github.com/jdcloudcom/cn/blob/edit/documentation/Cloud-Security/Advanced-Anti-DDoS/Pricing/Billing-Rules.md)

 