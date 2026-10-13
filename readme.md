# CozyLife DPID Description

**CozyLife uses the key-value in json format to describe status information. This document explains the meaning of key and value in different product categories. For example, the switch state in electrical equipment is on, and the following json data can be used to represent**
```
{
     "1":1
}
```


A Data Point Identifier (DPID) ranges from 1 to 255. Identifiers 1–100 have fixed meanings within a product type; the same identifier may have different meanings in different product types.

The meaning of identifiers 101–255 can vary by Product Identifier. Before using these identifiers, confirm the definitions for the specific product. The definitions listed by category apply only to products that use them.

#### [中文](./readme_zh.md) [English](./readme.md)

- [Lighting](./light_en.md) · [中文](./light_zh.md)
- [Electrician](./electrician_en.md) · [中文](./electrician_zh.md)
- [Motor](./motor_en.md) · [中文](./motor_zh.md)
- [Sensor](./sensor_en.md) · [中文](./sensor_zh.md)
- [Small appliance](./appliance_en.md) · [中文](./appliance_zh.md)
- [Energy storage battery](./battery_en.md) · [中文](./battery_zh.md)
- [Passthrough device](./passthrough_en.md) · [中文](./passthrough_zh.md)
- [Gateway](./gateway_en.md) · [中文](./gateway_zh.md)
- [Training device (pet collar)](./pet_trainer_en.md) · [中文](./pet_trainer_zh.md)
- [Video doorbell](./doorbell_en.md) · [中文](./doorbell_zh.md)



###TODO
- protocol header document
- cmd documentation
