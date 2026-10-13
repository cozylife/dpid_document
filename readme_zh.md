# CozyLife DPID描述

**CozyLife使用json格式的key-value描述状态信息，该文档说明了在不同产品品类中key、value的含义。例如在电工设备中的开关状态为开，可以使用以下json数据表示**
```
{
    "1":1
}
```


Data Point Identifier（功能点标识符，DPID）的编号范围为 1–255。编号 1–100 的含义在同一产品类型内固定；不同产品类型中的相同编号可能有不同含义。

编号 101–255 的含义可以随 Product Identifier（产品标识符）变化。使用这些编号前，请核对具体产品的定义；本目录按品类列出的定义仅适用于采用该定义的产品。

#### [中文](./readme_zh.md) [英文](./readme.md)

- [照明](./light_zh.md) · [English](./light_en.md)
- [电工](./electrician_zh.md) · [English](./electrician_en.md)
- [电机](./motor_zh.md) · [English](./motor_en.md)
- [传感](./sensor_zh.md) · [English](./sensor_en.md)
- [生活小电器](./appliance_zh.md) · [English](./appliance_en.md)
- [储能电池](./battery_zh.md) · [English](./battery_en.md)
- [透传设备](./passthrough_zh.md) · [English](./passthrough_en.md)
- [网关](./gateway_zh.md) · [English](./gateway_en.md)
- [训导类（宠物项圈）](./pet_trainer_zh.md) · [English](./pet_trainer_en.md)
- [可视门铃](./doorbell_zh.md) · [English](./doorbell_en.md)



### TODO
- 协议头文档
- cmd文档
