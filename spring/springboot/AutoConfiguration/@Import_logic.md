## 调用逻辑

![@Import 调用方式](/img/import_logic.png)

## 解析

#### 为什么只支持`ImportSelector` ，`ImportBeanDefinitionRegistrar` 和 `@Configuration`

如下图代码

```java
if (candidate.isAssignable(ImportSelector.class)) {
   // Candidate class is an ImportSelector -> delegate to it to determine imports
...
}
else if (candidate.isAssignable(ImportBeanDefinitionRegistrar.class)) {
   // Candidate class is an ImportBeanDefinitionRegistrar ->
   // delegate to it to register additional bean definitions   Class<?> candidateClass = candidate.loadClass();
...
}
else {
   // Candidate class not an ImportSelector or ImportBeanDefinitionRegistrar ->
   // process it as an @Configuration class   this.importStack.registerImport(
         currentSourceClass.getMetadata(), candidate.getMetadata().getClassName());
   processConfigurationClass(candidate.asConfigClass(configClass), exclusionFilter);
}
```

#### TODO
