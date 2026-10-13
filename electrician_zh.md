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
|  26   |    增加电量    |     add_ele      |     只读     |   number   |       否       |                       数值范围：0-50000，原始值步进：100；单位：kW·h；缩放参数：3，换算公式待确认                        |
|  27   |    当前电流    |   cur_current    |     只读     |   number   |       否       |                                  数值范围：0-30000,单位：mA                                  |
|  28   |    当前功率    |    cur_power     |     只读     |   number   |       否       |                                  数值范围：0-80000,单位：W                                   |
|  29   |    当前电压    |   cur_voltage    |     只读     |   number   |       否       |                                   数值范围：0-5000,单位：V                                   |
|  30   |    故障告警    |      fault       |     只读     |    enum    |       否       |                    故障内容：ov_cr, ov_vol, ov_pwr, ls_cr, ls_vol, ls_pow                    |
|  31   |    网络唤醒    |   wake_on_lan    |     只写     |    enum    |       否       |           Value：MAC:PORT  `MAC`长度12位,`PORT`为端口号(默认9) Eg:`4C34882C2CD9:9`           |
|  32   |    过电保护    |  power_protect   |     双向     |   number   |       否       |                               数值范围：0-1；0：取消过电保护；1：含义待确认                                |
|  33   |    无线按钮1    |  wireless_button1   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  34   |    无线按钮2    |  wireless_button2   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  35   |    无线按钮3    |  wireless_button3   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  36   |    无线按钮4    |  wireless_button4   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  37   |    无线按钮5    |  wireless_button5   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  38   |    无线按钮6    |  wireless_button6   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  39   |    无线按钮7    |  wireless_button7   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击           |
|  40   |    无线按钮8    |  wireless_button8   |     只上报     |   enum   |       是       |                               数值范围：0-3，0：长按， 1: 单击， 2: 双击， 3: 三击          |
|   41   |   剩余电量    |   battery    |     只读     |   number   |       是       | 数值范围：0至1000, 单位：千分比 |
|   42   |   总耗电量    |   total_ele    |     只读     |   number   |       是       |int类型，实际值=数值÷1000，单位：kWh，例如100表示0.1kWh |
|   43   | 清除总耗电量  |   cls_total_ele    |     只写     |   number   |       是       |int类型：1：清除历史累计总电量 |
|44|一路开关|switch_channel1|读写|enum|否|1：开；0：关|
|45|二路开关|switch_channel2|读写|enum|否|1：开；0：关|
|46|三路开关|switch_channel3|读写|enum|否|1：开；0：关|
|47|四路开关|switch_channel4|读写|enum|否|1：开；0：关|
|48|五路开关|switch_channel5|读写|enum|否|1：开；0：关|
|49|六路开关|switch_channel6|读写|enum|否|1：开；0：关|
|50|七路开关|switch_channel7|读写|enum|否|1：开；0：关|
|51|八路开关|switch_channel8|读写|enum|否|1：开；0：关|
|52| 开关1点动时间| key1_inch_tick| 双向| number| 否| 设置点动时间(s)|
|53| 开关1点动使能| key1_inch_enable| 双向| number| 否| 使能点动模式|
|54| 开关2点动时间| key1_inch_tick| 双向| number| 否| 设置点动时间(s)|
|55| 开关2点动使能| key1_inch_enable| 双向| number| 否| 使能点动模式|
|56| 开关3点动时间| key1_inch_tick| 双向| number| 否| 设置点动时间(s)|
|57| 开关3点动使能| key1_inch_enable| 双向| number| 否| 使能点动模式|
|58| 开关4点动时间| key1_inch_tick| 双向| number| 否| 设置点动时间(s)|
|59| 开关4点动使能| key1_inch_enable| 双向| number| 否| 使能点动模式|
|60| 开关5点动时间| key1_inch_tick| 双向| number| 否| 设置点动时间(s)|
|61| 开关5点动使能| key1_inch_enable| 双向| number| 否| 使能点动模式|
|62| 开关6点动时间| key1_inch_tick| 双向| number| 否| 设置点动时间(s)|
|63| 开关6点动使能| key1_inch_enable| 双向| number| 否| 使能点动模式|
|64| 开关7点动时间| key1_inch_tick| 双向| number| 否| 设置点动时间(s)|
|65| 开关7点动使能| key1_inch_enable| 双向| number| 否| 使能点动模式|
|66| 开关8点动时间| key1_inch_tick| 双向| number| 否| 设置点动时间(s)|
|67| 开关8点动使能| key1_inch_enable| 双向| number| 否| 使能点动模式|
|68| 功率限制| power_protect| 双向| number| 否| 过载功率(W)|
|69| 功率限制模式选择| power_protect_mode| 双向| enum| 否| 过载保护模式选择<br />`0`:关闭<br />`1`:高触发<br />`2`:低触发|
|70| 节能模式设置| energy_save_wh| 双向| number| 否| 单位：Wh（待确认）；缩放参数：3，换算公式待确认|
|71| 节能模式使能| energy_save_en| 双向| number| 否| 节能模式使能：`0`:关闭、`1`:开启|
|72|开关关闭原因|close_reason|只读|enum|否|开关关闭的原因，只在开关关闭后才刷新，打开开关不会更新此值<br>`0`: 系统关闭(如配置上电状态为关时上电触发的关闭，或苹果Home控制)<br>`1`:通过按键或翘板开关关闭<br>`2`:过流保护<br>`3`:定时器<br>`4`:倒计时<br>`5`:云控制<br>`6`:遥控器<br>`16`:功率限制<br>`17`:节能模式<br>`18`:点动模式<br>|
|73|功率限制触发时间|power_protect_time|双向|number|否|功率在设定的阈值范围内保持多长时间后触发动作(单位：100ms，如10表示1s)|
|74|节能模式实际触发值|energy_save_trig|只读|number|否|在总电量到达此值时触发节能模式，单位(Wh)|
| 101  | 查询433遥控列表   | key_map     | 只读         | string     | 否             | 返回key list  <br />`{"1":{"c":0,"f":1},"2":{"c":1,"f":0}}`<br />`1`、`2`为key_id;<br />`c`开关通道，`0`表示总控，其他数字表示对应开关通道，总控时，只能单选开或关，无翻转功能<br />`f`为功能，枚举型`0:关`、`1:开`、`2:翻转`、`3：无功能` |
| 102  | 433按键功能       | key_func    | 只写         | number     | 否             | 数值范围：0x0000~0xFFFF<br />转换为FF,FF,其中第一个字节表示按键ID，第二个字节表示按键功能，功能定义参考101：f |
| 103  | 433按键通道       | key_channel | 只写         | number     | 否             | 数值范围：0x0000~0xFFFF<br />转换为FF,FF,其中第一个字节表示按键ID，第二个字节表示通道，通道参考101：c |
| 104  | 學習433按鍵       | key_learn   | 只写         | enum       | 否             | 0：取消学习<br />1：开始学习                                 |
| 105  | 删除433按键       | key_del     | 只写         | number     | 否             | 删除的按键的id                                               |
