# 计网Ch8-公开密钥

...

## 验证交易网页是否是真实的网页而不是钓鱼网站
- 使用**证书（CA）**：server提供一个public key，client这边根据CA重新算一遍public key，如果对上就是真的。 
- 如果对当前CA不能相信呢？那就去找CA树上的父节点CA，一直追溯到自己信任的CA。
- PKI(Public-Key Infrastructures)

## 通信的安全性
- IPsec:确保信息的完整性
协议有：
	- AH认证头
		- 对数据不加密，主要进行**数据完整性检查**
		- 包括HMAC
		- 防止重发
	- ESP封装的安全数据
		- 传输模式下
		- 隧道模式下
		- 不管哪种都是**加密**的，安全性最高
- Firewalls
	- 架构：两个过滤，一个应用网关
- VPN

## 鉴别协议
- 基于共享秘密密钥的鉴别
	- 原则：一方发送一个随机数给另一方，后者以另一种方式把随机数发回去（查询-应答系统）
	- 密钥只有两方知道
	- 但可以用**反射攻击**来把这个协议干掉

## 网络攻击
