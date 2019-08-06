### 信任关系验证失败原因排查

1.如果用户将目录服务建立在云上，需要将目录服务和信任域部署在同一个VPC内。

2.如果用户是远程域或者是本地域，需要建立专线与目录服务的VPC打通，通信正常之后开始配置信任关系。

3.同一个VPC如果无法建立信任关系，请查看VPC的安全组是否将必须的端口开放。

4.在配置信任关系时建议将域控制实例上的防火墙关闭。