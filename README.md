# 自动刷电信网关脚本 #

### 用法： ###

1. 连接上 ChinaNet 无线网
2. 运行 运行.bat
3. 输入正确的电话号码即可
4. 通过运行 **刷新 IP.bat** 可更新计算机的 IP 地址
4. 通过运行 **检查更新.bat** 可获取脚本最新版本

### 提示： ###

1. 目前只在**北京化工大学**测试通过，其它地区不能保证能用
2. 由于电信服务器问题，可能出现第一次登录失败的情况，脚本会在**三秒后**执行第二次登录尝试，**两次登录都失败则进行下一组计算**
3. 默认十秒（由于北化网络不稳定）后开始检查网络连接，每十秒检测一次，直到网络断开
4. 由于电信服务器限制，同一 IP 获取 50 次以后会出现今天申请次数过多，届时请运行 **刷新 IP.bat**
5. 程序为 **Windows 64 位版本**，Windows 32 位版本或其它系统的请到 [http://nodejs.org/](http://nodejs.org/ "Node.js") 下载对应的 node.js 程序，然后在 shell 中运行 `node mother.js`

### 原理： ###

由于每次申请购买时长卡会得到**十分钟**的连接时间，便通过 node.js 模拟购买流程，以达到自动续网的目的。

![](http://www.processon.com/chart_image/54007b3d0cf2c2cdf4572bb1.png)

### 已知错误： ###

1. 一定概率重复出现**购物车为空**
2. 进程**重启后**无法请求得到 cookie

### 版权： ###

北京化工大学-学生网络中心-系统组 @Dolphin,   
MIT Licensed.
