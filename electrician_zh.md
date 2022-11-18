### 开关类功能点定义

| DPID  |     功能点     |      标识符      | 数据传输类型 | 功能点类型 | 是否支持自动化 |                                          功能点属性                                          |
| :---: | :------------: | :--------------: | :----------: | :--------: | :------------: | :------------------------------------------------------------------------------------------: |
|   1   |      开关      |      switch      |     双向     |   number   |       是       | 数值范围：00~FF，转化为二进制为1111 1111<br/>其中每一位代表一路开关，最多支持8路开关同时设置 |
|   2   |  开关1倒计时   |   countdown_1    |     双向     |   number   |       否       |                                  数值范围：0-86400,单位：s                                   |
|   3   | 开关1周期定时  |  normal_time_1   |     双向     |   string   |       否       |                                                                                              |
|   4   |  开关2倒计时   |   countdown_2    |     双向     |   number   |       否       |                                  数值范围：0-86400,单位：s                                   |
|   5   | 开关2周期定时  |  normal_time_2   |     双向     |   string   |       否       |                                                                                              |
|   6   |  开关3倒计时   |   countdown_3    |     双向     |   number   |       否       |                                  数值范围：0-86400,单位：s                                   |
|   7   | 开关3周期定时  |  normal_time_3   |     双向     |   string   |       否       |                                                                                              |
|   8   |  开关4倒计时   |   countdown_4    |     双向     |   number   |       否       |                                  数值范围：0-86400,单位：s                                   |
|   9   | 开关4周期定时  |  normal_time_4   |     双向     |   string   |       否       |                                                                                              |
|  10   |  开关5倒计时   |   countdown_5    |     双向     |   number   |       否       |                                  数值范围：0-86400,单位：s                                   |
|  11   | 开关5周期定时  |  normal_time_5   |     双向     |   string   |       否       |                                                                                              |
|  12   |  开关6倒计时   |   countdown_6    |     双向     |   number   |       否       |                                  数值范围：0-86400,单位：s                                   |
|  13   | 开关6周期定时  |  normal_time_6   |     双向     |   string   |       否       |                                                                                              |
|  14   |  开关7倒计时   |   countdown_7    |     双向     |   number   |       否       |                                  数值范围：0-86400,单位：s                                   |
|  15   | 开关7周期定时  |  normal_time_7   |     双向     |   string   |       否       |                                                                                              |
|  16   |  开关8倒计时   |   countdown_8    |     双向     |   number   |       否       |                                  数值范围：0-86400,单位：s                                   |
|  17   | 开关8周期定时  |  normal_time_8   |     双向     |   string   |       否       |                                                                                              |
|  18   |  上电状态设置  |   relay_status   |     双向     |    enum    |       否       |                                    枚举值off, on, memory                                     |
|  19   | 指示灯状态设置 |    led_status    |     双向     |    enum    |       否       |                                    枚举值none, relay, pos                                    |
|  20   |    背光开关    | backlight_status |     双向     |    enum    |       否       |                                                                                              |
|  21   |      童锁      |    child_lock    |     双向     |    enum    |       否       |                                                                                              |
|  22   |  太阳能灯模式  |    mode_index    |     双向     |    enum    |       否       |                      数值范围：0-3，0：光控；1：节能；2：常规；3：冬天                       |  |  |
|  23   |    循环定时    |    cycle_time    |     双向     |   string   |       否       |                                                                                              |
|  24   |    随机定时    |   random_time    |     双向     |   string   |       否       |                                                                                              |
|  25   |    点动开关    |  switch_inching  |     双向     |   string   |       否       |                                                                                              |
|  26   |    增加电量    |     add_ele      |     只读     |   number   |       否       |                       数值范围：0-50000,间距：100, 倍数：3,单位：kW·h                        |
|  27   |    当前电流    |   cur_current    |     只读     |   number   |       否       |                                  数值范围：0-30000,单位：mA                                  |
|  28   |    当前功率    |    cur_power     |     只读     |   number   |       否       |                                  数值范围：0-80000,单位：W                                   |
|  29   |    当前电压    |   cur_voltage    |     只读     |   number   |       否       |                                   数值范围：0-5000,单位：V                                   |
|  30   |    故障告警    |      fault       |     只读     |    enum    |       否       |                    故障内容：ov_cr, ov_vol, ov_pwr, ls_cr, ls_vol, ls_pow                    |
|  31   |    网络唤醒    |   wake_on_lan    |     只写     |    enum    |       否       |           Value：MAC:PORT  `MAC`长度12位,`PORT`为端口号(默认9) Eg:`4C34882C2CD9:9`           |
|  32   |    过电保护    |  power_protect   |     双向     |   number   |       否       |                               数值范围：0-1，0：取消过电保护1                                |
|  33   |    无线按钮1    |  wireless_button1   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  34   |    无线按钮2    |  wireless_button2   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  35   |    无线按钮3    |  wireless_button3   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  36   |    无线按钮4    |  wireless_button4   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  37   |    无线按钮5    |  wireless_button5   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  38   |    无线按钮6    |  wireless_button6   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  39   |    无线按钮7    |  wireless_button7   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  40   |    无线按钮8    |  wireless_button8   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击          |
|   41   |   剩余电量    |   battery    |     只读     |   number   |       是       | 数值范围：0至1000, 单位：千分比 |