# Spring Cloud Dataway with Nacos

- 工程
    - spring-cloud-gateway
    - spring-cloud-consumer
    - spring-cloud-provider
- 特点
    - Hasor Dataway 接口配置信息保存在 Nacos
    - Spring Cloud 服务发现基于 Nacos
    - Hasor Dataway 连接了另外两个 MySQL 数据源
    - Dataway 服务在 provider 应用中注册了一个全新的服务名
- consumer
    - http://localhost:8081/echo/abc
    - http://localhost:8081/api/abc?message=HelloWord
- provider
    - http://localhost:8082/echo/abc (SpringMVC 原生服务)
    - http://localhost:8082/api/abc?message=Helloword (需要到Dataway里面新建)
    - http://localhost:8082/interface-ui/ (Dataway界面)
- gateway
    - http://localhost:8080/consumer/echo/abc (代理consumer)
    - http://localhost:8080/consumer/api/abc?message=HelloWord (代理consumer)
    - http://localhost:8080/provider/echo/abc (代理provider)
    - http://localhost:8080/dataway/api/abc?message=abc (代理 Dataway)
    - http://localhost:8080/dataway-ui/ (代理 Dataway Admin)
