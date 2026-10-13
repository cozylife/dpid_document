### Pet Collar (Training Device) DPID Definition

| DPID |       Function        |   Identifier    | Data Transfer Type | Data Type | Support Automation |                        Function Attributes                        |
| :--: | :-------------------: | :-------------: | :----------------: | :-------: | :----------------: | :---------------------------------------------------------------: |
|  2   |    Charging state     |  charge_state   |      Read-only     |   enum    |         No         |        Value range: 0-1; 0: not charging, 1: charging            |
|  3   |         Sound         |      sound      |    Bidirectional   |   enum    |         No         |            Value range: 0-1; 0: off, 1: on                       |
|  4   |       Vibration       |      vibra      |    Bidirectional   |   enum    |         No         |            Value range: 0-1; 0: off, 1: on                       |
|  5   |     Electric shock    |      shock      |    Bidirectional   |  number   |         No         |               Value range: 0-16;                                  |
|  6   |      Sensitivity      |   sensitivity   |    Bidirectional   |  number   |         No         |               Value range: 0-10;                                  |
|  7   |     Battery level     |     battery     |      Read-only     |  number   |         No         |         Value range: 0-1000, unit: per mille                      |
|  8   |     Auto bark stop    |      bark       |    Bidirectional   |   enum    |         No         |            Value range: 0-1; 0: off, 1: on                       |
|  9   |  Batch report 3,4,5   |      batch      |      Read-only     |  string   |         No         | [{time:1661326672,dpid:3,value:1},{time:1661326672,dpid:4,value:1}] |
|  10  |       Heartbeat       | mpaas_heartbeat |       One-way      |  number   |         No         | Value range: 1, 0. App online heartbeat: the app keeps sending 1 while in the foreground and may send 0 when hidden; if no message is received for a long time or 0 is received, the device determines that the app has exited |
