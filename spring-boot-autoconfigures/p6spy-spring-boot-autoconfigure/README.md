# p6spy-spring-boot-autoconfigure
Spring boot application integrates p6spy print logs quickly

p6spy：https://github.com/p6spy/p6spy


## Quick start




## Configure application.yml

```
spring:
  datasource:
    driver-class-name: com.p6spy.engine.spy.P6SpyDriver
    url: jdbc:p6spy:h2:mem:test
//  url: jdbc:p6spy:mysql://xxx
    username: xxx
    password: xxx


p6spy:
  config:
    enabled: true
    appender: com.p6spy.engine.spy.appender.Slf4JLogger
    logMessageFormat: com.p6spy.engine.spy.appender.CustomLineFormat
    customLogMessageFormat: 时间：%(currentTime) | SQL耗时： %(executionTime) ms | 连接信息： %(category)-%(connectionId) | 执行语句： %(sql)

```



## More p6spy configuration description

https://p6spy.readthedocs.io/en/latest/configandusage.html