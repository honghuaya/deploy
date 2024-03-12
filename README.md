# 主要介绍安全设备的部署方式与流程，以及相应的功能及模块

# 主要功能的实现 AF与AC进行联动 AF 8.0.26 | AC 12.0.44
1．AF以路由模式部署在网关，并配置接口区域，应用控制策略，地址转换，端口映射，静态路由。
2．AC以路由模式部署在核心转发区，做内网IP地址规划、PC及终端上网认证、应用过滤、流量管理。
3．为了保障内网服务器、PC及终端安全管理，在AF上配置内网Web安全，防DDoS攻击、SQL注入攻击，配置
安全限制，防僵尸网络、木马、蠕虫以及勒索病毒。在AC上配置AD域认证和上网权限限制、行为管控、行为审计。

# EDR与防火墙进行联动管控 AF 8.0.26 | EDR 3.5.18
1．EDR管理平台以云端的方式部署，获取agent，给内网终端分配组别，便于管理。以静默安装的方式，将agent
分别安装到内网终端，通过云端管理平台可以扫描到未安装agent的终端。
2．为了更好的防护内网终端安全，分别配置实时防护、勒索防护、可信进程、自动隔离可疑shell。配置漏洞防护策略，
并开启威胁检测的终端基线检查。配置微隔离策略，并开启为隔离和流量上报。
3．为了更有效的管理内网终端，通过策略中心，开启防退出、防卸载功能，并开启定时查杀病毒功能（也可随时查杀）。
