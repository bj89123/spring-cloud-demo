此Demo主要围绕Spring Cloud “全家桶”展开，包含Eureka 客户端、 Eureka 注册中心、 Eureka 服务网关。
### 使用步骤
1. 进入项目spring-cloud-eureka-server，启动注册中心项目
2. 进入项目spring-cloud-eureka-client，执行命令mvn clean package 打包
3. 启动两个客户端实例
```
java -jar spring-cloud-eureka-client-0.0.1-SNAPSHOT.jar --server.port=8001 --spring.application.name=eureka-client
java -jar spring-cloud-eureka-client-0.0.1-SNAPSHOT.jar --server.port=8002 --spring.application.name=eureka-client
```
4. 进入项目spring-cloud-gateway，启动服务网关项目
5. 访问**127.0.0.1/api/index** 即可通过网关访问客户端实例
