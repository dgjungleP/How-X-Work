# 用途
可以为自己制作的功能更好的接入到 `springboot`的生态中使用。

## 主要控件
- @AutoConfigurationPackage
- AutoConfigurationPackages.Registrar
- @Import
> 1. 带有@Configuration的配置类 (4.2版本之后可以导入普通类)
> 2. ImportSelector的实现
> 3. ImportBeanDedinitionRegistrar
> [More](@Import_logic.md)

- @AutoConfigurationPackage
- AutoConfigurationImportSelector

## 实现原理

### 手动注入的方式
> 使用 @Import 直接引用对应的Configuration类

### 自动注入的方式

> SpringBoot 使用的是[AutoConfigurationImportSelector](AutoConfigurationImportSelector.md)做到的实现