### Gateway DPID Definition

| DPID  |         Function          |  Identifier   | Data Transfer Type | Data Type | Support Automation |   Function Attributes    |
| :---: | :-----------------------: | :-----------: | :----------------: | :-------: | :----------------: | :----------------------: |
|   2   |      Discovery mode       |   discover    |    Bidirectional   |   enum    |         No         |     0: off, 1: on        |
|   3   |        Status LED         |  status_led   |    Bidirectional   |   enum    |         No         | 0: always off, 1: real-time, 2: always on |
|   4   |        WiFi LED           |   wifi_led    |    Bidirectional   |   enum    |         No         | 0: always off, 1: real-time, 2: always on |
|   5   |      Ethernet LED         |    eth_led    |    Bidirectional   |   enum    |         No         | 0: always off, 1: real-time, 2: always on |
|   6   |   Number of sub-devices   |   sdev_num    |      Read-only     |  number   |         No         |    Value range: 0-120    |
|   7   | Sub-device data version   | sdev_data_ver |      Read-only     |  number   |         No         |   Value range: 0-65535   |
