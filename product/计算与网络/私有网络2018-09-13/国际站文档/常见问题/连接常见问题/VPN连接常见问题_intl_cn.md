## 1. 一个VPC可以通过VPN连接与多个IDC互联么？
可以，目前私网网络可以建立VPN网关并在每个VPN网关上建立多个VPN通道，每个VPN通道可以打通一个本地IDC。

## 2. 两个VPC之间通信可以通过VPN连接实现吗？
可以，你需要分别在两个VPC内购买VPN网关、配置VPN通道和对端网关，但配置较为复杂，建议您使用对等连接。对等连接使用腾讯骨干网连接两个VPC，其通信质量更有保障。

## 3. 通过VPN连接的私有网络和IDC之间的网络质量如何保证
- 私有网络与IDC之间走的是公网，依赖公网网络的质量,可能会出现时延、丢包、抖动，如果您需要更加稳定的通信质量，建议您使用专线接入服务。
- VPN后台会全天监控网络质量，包括keepalive和网络时延，如果出现网络异常情况会请运维及时处理。您也可以在控制台实时监控VPN网关和通道的流量状态，如果发现异常及时与我们联系。

## 4. VPN通道未联通可能原因？
- 对端网关出现故障
- 通道配置错误
- 通道长时间没有流量
