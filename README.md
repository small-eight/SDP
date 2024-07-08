# SDP
SDP(Software Defined Perimeter)即“软件定义边界”，是基于零信任（Zero Trust）理念的新一代网络安全模型。<br>
可以实现网络完全隐身，无需开放任何TCP端口，让企业服务从互联网上“隐身”，不为潜在攻击者提供任何端口扫描和攻击的机会。<br>
SDP主要用到了[SPA单包认证技术](https://github.com/small-eight/spa)，实现无连接的授权以及端口保护<br>
## 说明


## 使用
SDP主要分为了:<br>
sdp_clinet.py 作为客户端，发起发送认证信息给controller<br>
sdp_gateway.py 作为网关，接受controller策略，响应主机访问<br>
sdp_controller.py 作为控制器，接受用户的认证信息，并下发相应策略给gateway开放访问<br>

sdp针对不同业务模式，有多种部署模式<br>
这里只推荐sdp作为统一转发网关模式，该模式下所有流量都会经过gateway进行转发。
   
client->servers，服务器部署sdp_gateway.py，作为AH接受客户端的连接。<br>
client-gateway(部署sdp_gateway.py)-servers 推荐此模式，即通过统一网关对受保护的服务器进行访问。<br>
推荐模式下
