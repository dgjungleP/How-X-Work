## 命名
> 请使用规则\<mypluginName\>-maven-plugin

##  引入依赖

``` java
<dependencies>  
    <dependency> 
        <groupId>org.apache.maven</groupId>  
        <artifactId>maven-plugin-api</artifactId>  
        <version>3.6.3</version>  
    </dependency>    
    <dependency>        
	    <groupId>org.apache.maven.plugin-tools</groupId>  
        <artifactId>maven-plugin-annotations</artifactId>  
        <version>3.5.2</version>  
    </dependency>
</dependencies>
```

## 指定打包方式
> 打包方式要设置为`maven-plugin`


## 创建Mojo
> 实现`AbstractMojo`，并使用`@Mojo`注解进行标注

## 使用mvn新建插件
``` shell
mvn archetype:generate \
  -DgroupId=sample.plugin \
  -DartifactId=hello-maven-plugin \
  -DarchetypeGroupId=org.apache.maven.archetypes \
  -DarchetypeArtifactId=maven-archetype-plugin
```