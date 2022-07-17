# CloudWeGo 源码解读

[CloudWeGo](https://github.com/cloudwego) 是字节跳动基础架构团队开源出来的项目，它是一套可快速构建企业级云原生架构的中间件集合，它专注于微服务通信与治理，具备高性能、可扩展、高可靠的特点，且关注易用性。

主要项目：
- Kitex：高性能、强可扩展的 Golang RPC 框架
- Netpoll：高性能、I/O 非阻塞、专注于 RPC 场景的网络框架
- Thriftgo：Golang 实现的 Thrift 编译器，支持插件机制和语义检查
- Netpoll-http2：基于 Netpoll 的 HTTP/2 实现
- Hertz：[həːts] Golang 微服务 HTTP 框架

## Kitex

### 公开资料
- [github/cloudwego/kitex](https://github.com/cloudwego/kitex)
- [cloudwego.io/kitex](https://www.cloudwego.io/zh/docs/kitex/)
- [字节跳动微服务架构体系演进 - 成国柱](https://cloudwego.feishu.cn/docs/doccnyu0JEq4DiKwuKATn3MxIOf)
- [Go 组件设计与实现 - 掘金小册](https://juejin.cn/video/7046282096435789835)
- [字节杨芮：微服务框架 Kitex 的设计、实践及开源 - 得物技术分享](./files/微服务框架Kitex的设计实践及开源-杨芮.pdf)
- [Go 微服务框架 Kitex 扩展性设计和实践 | JTalk Meetup 11期](https://www.bilibili.com/video/BV1qa4y1H7i2)
- [CloudWeGo 社区对外 Meetup](https://github.com/cloudwego/community/tree/main/meetup)

### 整体性设计
- [从 CloudWeGo 谈云原生时代的微服务与开源](https://mp.weixin.qq.com/s/xWxb84WkYtWTBoVV3mzs6g)
- Kitex 模块划分及调用链路
- Kitex 扩展性设计
- Kitex 设计思想

### 服务治理
- 服务注册与发现
- 熔断
- [限流](https://xie.infoq.cn/article/408cd95d469ee2cdc72c1cd10)
- 请求重试
- 负载均衡


### 公共模块
- rpcinfo
- endpoint
- middleware

### remote

remote 模块是 Kitex 实现的 RPC 核心，是与远端交互的重要模块。

- transport pipeline
- trans handler
- codec
- payloadCodec
