springdoc-bootstrap-ui
=========================
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.windpanda.doc/springdoc-bootstrap-ui/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.windpanda.doc/springdoc-bootstrap-ui)



## 简介

基于swagger-bootstrap-ui做了一些优化，打包成webjars。原地址是在 [swagger-bootstrap-ui](https://github.com/xiaoymin/Swagger-Bootstrap-UI)




## 使用

1. 引入ui包

```xml
<dependency>
  <groupId>com.windpanda.doc</groupId>
  <artifactId>springdoc-bootstrap-ui</artifactId>
  <scope>runtime</scope>
  <version>${latestVersion}</version>
</dependency>
```

2. 设置静态资源

```java
@Configuration
public class SpringDocConfig implements WebFluxConfigurer {

    @Override
    public void addResourceHandlers(ResourceHandlerRegistry registry) {
        registry.addResourceHandler("/springdoc-ui/**").addResourceLocations("classpath:/META-INF/resources/webjars/springdoc-bootstrap-ui/");
    }
}

```

3. 访问地址
```html
http://127.0.0.1/springdoc-ui/index.html
```



再次声明 原作者 : [xiaoymin](https://github.com/xiaoymin/Swagger-Bootstrap-UI)

该项目只是基于原基础上进行了一些改造,非常感谢原作者的开源项目节省了大量的研发成本。
