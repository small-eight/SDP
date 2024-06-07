# SDP
SDP(Software Defined Perimeter)即“软件定义边界”，是基于零信任（Zero Trust）理念的新一代网络安全模型。<br>
可以实现网络完全隐身，无需开放任何TCP端口，让企业服务从互联网上“隐身”，不为潜在攻击者提供任何端口扫描和攻击的机会。<br>
SDP中主要用到了[SPA单包认证技术](https://github.com/small-eight/spa)。<br>
## 说明
SDP模型主要分为了:<br>
(1)Initiating SDP Host，即IH发起连接的客户端；<br>
(2)Accepting SDP Host，即AH接受连接的主机；<br>
(3)SDP Controller，即控制器。<br>

sdp_clinet.py 作为IH发起访问<br>
sdp_gateway.py 作为AH接受主机访问<br>
sdp_controller.py 作为控制器<br>

## 使用
