# SDP
Software Defined Perimeter python realize<br>
SDP(Software Defined Perimeter)即“软件定义边界”，是基于零信任（Zero Trust）理念的新一代网络安全模型。<br>
SDP模型主要分为了:
(1)Initiating SDP Host，即IH发起连接的客户端；<br>
(2)Accepting SDP Host，即AH接受连接的主机；<br>
(3)SDP Controller，即控制器。<br>
SDP中主要用到了[SPA单包认证技术](https://github.com/small-eight/spa)。
## 说明
sdp_clinet.py 作为IH发起访问<br>
sdp_gateway.py 作为AH接受主机访问<br>
sdp_controller.py 作为控制器<br>

## 使用
