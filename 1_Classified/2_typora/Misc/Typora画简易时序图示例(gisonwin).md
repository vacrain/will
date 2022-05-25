```sequence
Title:网关鉴权时序图(By GisonWin) 
客户端->网关:将公共参数和accessKey发送给网关
网关->注册中心:网关将本身作为服务注册到注册中心
Note right of 网关:通过参数和accessKey生成秘钥匙对
网关->Redis:保存秘钥对,并设计过期时间
Redis-->网关:
网关->客户端:返回秘钥对
Note right of 客户端:使用秘钥对所有参数md5生成签名
客户端->网关:调用接口携带参数,公钥和签名
Note over 注册中心: 服务A1
网关->Redis:根据公钥查私钥
Redis->网关:返回私钥
网关->客户端:私钥为空,返回秘钥过期code,客户端重新获取秘钥
Note right of 网关:使用秘钥对参数进行md5 验签
网关->客户端:验签失败返回错误码
网关->注册中心:验签成功调用注册中心的服务
Note over 注册中心: 服务A2
Note over 注册中心: 服务A3
注册中心-->网关:
Note over 注册中心: 服务A4
网关->客户端:返回结果
participant 服务
服务-->注册中心:注册到注册中心
注册中心-->服务:定时检查服务是否存活
```

---

```mermaid
%% gateway validate of sequence diagram ->直线 -->虚线  ->> 实线箭头 -->>虚线箭头
  sequenceDiagram
  Title:Author:GisonWin(gisonwin@qq.com)
  participant 客户端
  participant 网关
  participant 注册中心
  participant 下游服务
   网关-->>注册中心:网关将自身注册到注册中心
   Note over 注册中心: 网关服务
   注册中心-->>网关:定时检查网关服务是否正常提供服务
   下游服务-->>注册中心:服务将自身注册到注册中心
   Note over 注册中心: 下游服务A2
   注册中心-->>下游服务:定时检查下游服务是否正常提供服务
   客户端->>网关: 客户端携带token信息访问网关
   loop 检查
        网关->>网关:token/blacklist验证
   end
   alt has token
   网关-->>注册中心:根据token路由注册中心的服务
   注册中心-->>网关:服务将处理结果返回给网关
   网关-->>客户端:网关将结果返回给客户端
   else no token
   网关-->>客户端:未发现携带有效的身份信息
   网关-->>客户端:您在当前的黑名单中,请稍后重试
   end
 
```

​                                                                                                                                                                  by <a href="mailto:gisonwin@qq.com">GisonWin</a>