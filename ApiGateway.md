## 定义   
负责将服务以API的形式暴露（给系统外部），以实现业务功能  north-south[<sup>1</sup>](#refer)  
ps：微网关（microgateway）处理内部微服务间的调用 east-west[<sup>2</sup>](#refer)  
## 功能[<sup>2</sup>](#refer)     
1.请求权限认证  
2.请求路由转发  
3.请求流量控制  
4.处理DDoS攻击  
5.处理错误和异常  
6.服务请求熔断  
## 传统API网关问题  
1.传统配置信息（路由，限速数据...）需要绑定到二进制文件或持久化到数据库，存在时延，阻塞的存在。[<sup>2</sup>](#refer)    
2.数据层面（data plane）和API应用控制器（control plane）紧耦合，造成API控制逻辑出现异常会影响到路由处理功能。[<sup>2</sup>](#refer)    
3.因为功能过于强大，造成资源占有量达。[<sup>2</sup>](#refer)   





















<div id="refer"></div>  

## Reference  
1.[Service Mesh和API Gateway关系深度探讨](https://mp.weixin.qq.com/s/XPJS1C121l5Wkpp7SQJfnQ)  
2.[Do You Really Need Different Kinds of API Gateways?](https://www.nginx.com/blog/do-you-really-need-different-kinds-of-api-gateways-hint-no/)  
