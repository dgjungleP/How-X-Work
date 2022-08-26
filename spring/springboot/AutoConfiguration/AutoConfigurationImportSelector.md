## 核心

> 遵从 SPI 原则，默认从`META-INF/spring.factories`路径中去获取 Class 类的全路径

## 步骤

1. 从指定的路径中获取到 class 类的全路径
2. 去除重复的 class 类全路径
3. 从注解中获取到需要排除的和需要过滤的 class
