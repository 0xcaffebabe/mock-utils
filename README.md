# mock-utils

mock some dto

## use

```java
// 一个填充了随机数据的dto
DTO dto = MockUtils.create(DTO.class);
// DTO{name='arg01879', id=4974244006328130353, createtime=2020-05-09T21:17:18.028795300}
// 随机数据的dto的list
var list = MockUtils.create(DTO.class,10);
// [DTO{name='arg014343', id=325138898443134940, createtime=2020-05-09T21:17:18.028795300}, ...
```

## extend

```java
static {
    ...
    generatorMap.put(Type.class,new CustomGenerator());
}
class CustomGenerator implements Generator<Type> {
    Type generate(Parameter parameter){
        // return your mock object
    }
} 
```