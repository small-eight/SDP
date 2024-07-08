# SDP
SDP(Software Defined Perimeter)即“软件定义边界”，是基于零信任（Zero Trust）理念的新一代网络安全模型。<br>
可以实现网络完全隐身，无需开放任何TCP端口，让企业服务从互联网上“隐身”，不为潜在攻击者提供任何端口扫描和攻击的机会。<br>
SDP主要用到了[SPA单包认证技术](https://github.com/small-eight/spa)，实现无连接的授权以及端口保护<br>
## 说明


## 使用
SDP主要分为了:<br>
(1)Initiating SDP Host，即IH发起连接的客户端；<br>
(2)Accepting SDP Host，即AH接受连接的主机；<br>
(3)SDP Controller，即控制器;<br>
(4)SDP Identify,即认证器.<br>

sdp_clinet.py 作为客户端对应IH发起访问<br>
sdp_gateway.py 作为AH接受主机访问<br>
sdp_controller.py 作为控制器<br>
sdp_identify.py 作为认证器<br>


sdp有多种部署模式<br>
1. 合并部署
   gateway与controller部署在一起
2. 分布式部署
   
client->servers，服务器部署sdp_gateway.py，作为AH接受客户端的连接。<br>
client-gateway(部署sdp_gateway.py)-servers 推荐此模式，即通过统一网关对受保护的服务器进行访问。<br>
推荐模式下
