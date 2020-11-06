## 定义   
负责将服务以API的形式暴露（给系统外部），以实现业务功能  north-south[<sup>1</sup>](#refer)  
ps：微网关（microgateway）处理内部微服务间的调用 east-west[<sup>2</sup>](#refer)  
APIGateway解决了外部调用端直接调用服务API的问题，无需了解微服务内部架构，解耦了第三方程序和本为服务耦合度...[<sup>4</sup>](#refer)  
服务API  公共API（API Gateway）    
## 功能[<sup>2</sup>](#refer)     
1.请求权限认证[<sup>2</sup>](#refer)  
2.请求路由转发[<sup>2</sup>](#refer)  
3.请求流量控制[<sup>2</sup>](#refer)  
4.处理DDoS攻击[<sup>2</sup>](#refer)  
5.处理错误和异常[<sup>2</sup>](#refer)  
6.服务请求熔断[<sup>2</sup>](#refer)  
7.服务与数据管理[<sup>3</sup>](#refer)    
* 基于注册中心服务配置和发现  
* 订阅/通知机制,通过注册中心的订阅/通知机制实现数据的及时更新  
* 服务治理，一方面通过业务数据的维护，控制请求流量及可访问的服务范围；另一方面通过注册中心及时感知后端服务API的状态变化    

8.安全检查  流量控制/权限控制/请求校验/报文处理[<sup>3</sup>](#refer)      
9.动态路由[<sup>3</sup>](#refer)      
* 多维度服务路由，通过多维度路由规则配置实现服务识别能力  
* 异步通信，通过异步通信机制实现高效交互能力  
* 服务降级熔断，通过服务隔离，实现自动化服务降级和断路能力  

10.监控 日志记录/指标收集分析/监控报警[<sup>3</sup>](#refer)      
11.API生命周期管理[<sup>3</sup>](#refer)    
12.主功能</span>[<sup>4</sup>](#refer)：  
* 请求路由：关键功能，将请求路由到相应的服务来实现一些API操作，典型的反向代理特性。    
* API组合：将特定多服务API请求组合成单一API请求，对外部提供给。    
* 协议转换：将微服务内部不同的协议转换向外提供统一协议，例如 gRPC、REST--->RESTful API     

13.边缘功能，在应用程序边缘实现的请求、处理功能</span>[<sup>4</sup>](#refer)：  
* 身份验证：验证发出请求的客户端身份    
* 访问授权：验证客户端是否有权执行该特定操作    
* 速率限制：限制特定客户或所有客户端每秒的请求数    
* 缓存：缓存响应以减少对服务的请求次数  
* 指标收集：收集有关API使用情况的指标，已进行计费分析    
* 请求日志：记录请求历史  
## 传统API网关问题  
1.传统配置信息（路由，限速数据...）需要绑定到二进制文件或持久化到数据库，存在时延，阻塞的存在。[<sup>2</sup>](#refer)    
2.数据层面（data plane）和API应用控制器（control plane）紧耦合，造成API控制逻辑出现异常会影响到路由处理功能。[<sup>2</sup>](#refer)    
3.因为功能过于强大，造成资源占有量达。[<sup>2</sup>](#refer)   





















<div id="refer"></div>  

## Reference  
1.[Service Mesh和API Gateway关系深度探讨](https://mp.weixin.qq.com/s/XPJS1C121l5Wkpp7SQJfnQ)  
2.[Do You Really Need Different Kinds of API Gateways?](https://www.nginx.com/blog/do-you-really-need-different-kinds-of-api-gateways-hint-no/)  
3.[恒丰银行分布式核心系统 -API 网关技术原型落地实践](./resource/gateway/恒丰银行分布式核心系统_API网关技术原型落地实践.pdf)  
4.[apigateway-pattern](https://microservices.io/patterns/apigateway.html)   
