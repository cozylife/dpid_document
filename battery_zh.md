### 储能电池类功能点定义

| DPID  |      功能点      |           标识符            | 数据传输类型 | 功能点类型 | 是否支持自动化 |                      功能点属性                       |
| :---: | :--------------: | :-------------------------: | :----------: | :--------: | :------------: | :---------------------------------------------------: |
|   1   |       开关       |        switch_power         |     双向     |   number   |       否       |数值范围：0000~FFFF，转化为二进制为1111 1111 1111 1111 其中每一位代表一路开关，最多支持16路开关同时设置|
|   2   | 储蓄电源当前状态 |       current_status        |     只读     |   number   |       否       |               枚举值 0关机 1充电 2放电                |
|   3   |   电池剩余电量   |           battery           |     只读     |   number   |       否       |                数值范围：0-100,单位：%                |
|   4   |    总输出功率    |        total_output         |     只读     |   number   |       否       |          数值范围：0-3000（待确认），单位：W           |
| 5-20  |   支路输出功率   |         output1-16          |     只读     |   number   |       否       |          数值范围：0-3000（待确认），单位：W           |
|  21   |    总输入功率    |        total_intput         |     只读     |   number   |       否       |          数值范围：0-3000（待确认），单位：W           |
| 22-29 |   支路输入功率   |          intput1-8          |     只读     |   number   |       否       |          数值范围：0-3000（待确认），单位：W           |
|  30   |   剩余可用时间   |   residue_available_time    |     只读     |   number   |       否       |              数值范围：0-65535,单位：min              |
|  31   |   剩余充电时间   |    residue_charging_time    |     只读     |   number   |       否       |              数值范围：0-65535,单位：min              |
|  32   |   电池温度(K)    |        battery_temp         |     只读     |   number   |       否       | 数值范围：0-500，单位：K，例如 303K 表示 30℃ |
|  33   |    照明灯模式    |       floodlight_mode       |     双向     |   number   |       否       |                        枚举值                         |
|  34   |    照明灯亮度    |        floodlight_v         |     双向     |   number   |       否       |                   数值范围：1-1000                    |
|  35   |     LED 模式     |          led_mode           |     双向     |   number   |       否       |                        枚举值                         |
|  36   |     LED 颜色     |            led_h            |     双向     |   number   |       否       |                数值范围：0-360 或 FFFF                |
|  37   |     LED 色度     |            led_s            |     双向     |   number   |       否       |               数值范围：0-1000 或 FFFF                |
|  38   |     LED 色温     |            led_t            |     双向     |   number   |       否       |               数值范围：0-1000 或 FFFF                |
|  39   |     LED 亮度     |            led_v            |     双向     |   number   |       否       |                   数值范围：1-1000                    |
|  40   |     待机时间     |        standby_time         |     双向     |   number   |       否       |              数值范围：0-1440, 单位：min              |
|  41   |     息屏时间     |        led_down_time        |     双向     |   number   |       否       |              数值范围：0-65535, 单位：s               |
|  42   |      提示音      |           prompt            |     双向     |   number   |       否       |                      0关闭 1开启                      |
|  43   |     按键声音     |          key_sound          |     双向     |   number   |       否       |                      0关闭 1开启                      |
|  44   |      故障码      |         Fault code          |     只读     |   number   |       否       |                    数值范围：0-FF                     |
|  45   |   E-Turbo状态    |        E_Turbo_state        |     双向     |   number   |       否       |                    0不启用，1启用                     |
|  46   |   优先充电方式   |    Preferred_charge_mode    |     双向     |   number   |       否       |            0同时充电  1从机优先  2主机优先            |
|  47   |    AC快充功率    |     AC_fastinput_power      |     双向     |   number   |       否       |             数值范围：0-5000，分辨率：1W              |
|  48   |    AC慢充功率    |     AC_slowinput_power      |     双向     |   number   |       否       |             数值范围：0-5000，分辨率：1W              |
|  49   |  交流电待机时间  |       AC_standby_time       |     双向     |   number   |       否       |              数值范围：0-1440，单位：min              |
|  50   |   恢复出厂参数   |     Restore_parameters      |     双向     |   number   |       否       |             0保持现有参数  1恢复出厂参数              |
|  51   |  在线加电包个数  |   Battery_pack_online_num   |     只读     |   number   |       否       |                       范围0-15                        |
|  52   |  故障加电包编号  |   Battery_pack_fault_num    |     只读     |   number   |       否       |                       范围0-15                        |
|  53   | 加电包充电功率 | Battery_pack_input_power     |     只读     |   string   |       否       |        FFFFFFFF...FFFF: 15组FFFF，0000-FFFF：0-65535  |
|  54   | 加电包放电功率 | Battery_pack_output_power    |     只读     |   string   |       否       |        FFFFFFFF...FFFF: 15组FFFF，0000-FFFF：0-65535  |
|   55   |   电池剩余电量   |          batteryWH          |     只读     |   number   |       否       |          数值范围：待确认（剩余的实际电量），单位：WH           |
|  56   |   电池2温度(K)    |        battery_temp2_two         |     只读     |   number   |       否       | 数值范围：0-500，单位：K，例如 303K 表示 30℃ |
|  57   |   温度单位(℃/℉)    |        battery_temp_unit         |     双向     |   number   |       否       | 数值范围：0-1, 0：℃，1： ℉|
|  58   |    亮度档位    |        light_gear         |     双向     |   number   |       否       |                   数值范围：1、2、3                    |
|  59   |     LED 颜色(默认配色)     |            led_h_defaults           |     双向     |   number   |       否       |                数值范围：0/1                |
|  60   |     蜂鸣器开关     |            buzzer           |     双向     |   number   |       否       |                数值范围：0/1                |
|  61   |     AC电压设定     |            ac_voltage           |     双向     |   number   |       否       |                数值范围：0-3. 0：100V/50Hz或60Hz、1：120V/60Hz、2：240V/50Hz、3：230V/50Hz               |
|  62   |     DC电压设定     |            dc_voltage           |     双向     |   number   |       否       |                数值范围： 0：12V/24V              |
|  63   |     交流输出开关     |            ac_switch           |     双向     |   number   |       否       |                数值范围： 0/1              |
|  64   |     交流输出自动休眠     |            ac_output_sleep           |     双向     |   number   |       否       |                数值范围： 0/1              |
|  65   |     优先充电选择     |            priority_charging_selection           |     双向     |   number   |       否       |                数值范围： 0-2 'AC、DC、MPPT'             |
|  66   |     AC充电时间统计     |           ac_charge_time           |     只读     |   number   |       否       |                数值范围：             |
|  67   |     AC充电电量统计     |           ac_charge_power           |     只读     |   number   |       否       |                数值范围： 	          |
|  68   |     AC放电时间统计     |           ac_discharge_time           |     只读     |   number   |       否       |                数值范围：              |
|  69   |     AC放电电量统计     |           ac_discharge_power           |     只读     |   number   |       否       |                数值范围：              |
|  70   |     DC充电时间统计     |           dc_charge_time           |     只读     |   number   |       否       |                数值范围：             |
|  71   |     DC充电电量统计     |           dc_charge_power           |     只读     |   number   |       否       |                数值范围： 	          |
|  72   |     DC放电时间统计     |           dc_discharge_time           |     只读     |   number   |       否       |                数值范围：              |
|  73   |     DC放电电量统计     |           dc_discharge_power           |     只读     |   number   |       否       |                数值范围：              |
|  74   |     MPPT充电时间统计     |           mppt_charge_time           |     只读     |   number   |       否       |                数值范围：             |
|  75   |     MPPT充电电量统计     |           mppt_charge_power           |     只读     |   number   |       否       |                数值范围： 	          |
|  76   |     MPPT放电时间统计     |           mppt_discharge_time           |     只读     |   number   |       否       |                数值范围：              |
|  77   |     MPPT放电电量统计     |           mppt_discharge_power           |     只读     |   number   |       否       |                数值范围：              |
|  78   |  加电包剩余可用时间   | Battery_pack_output_time   |     只读     |   string   |       否       | 数值范围：0-65535,单位：min  |
|  79   |  加电包剩余电量   |           Battery_pack_surplus_power          |     只读     |   number   |       否       |                数值范围：0-100,单位：%              |
|  80   |  加电包温度   |           Battery_pack_temp         |     只读     |   number   |       否       |                数值范围：0-500            |
|  81   |     LED 灯条颜色     |           led_bar_h           |     双向     |   number   |       否       |                数值范围： 0-360           |
|  82   |     LED 灯条颜色色度     |           led_bar_s            |     双向     |   number   |       否       |               数值范围：0-1000 或 FFFF                |
|  83   |     LED 灯条颜色亮度     |           led_bar_v            |     双向     |   number   |       否       |                   数值范围：1-1000                    |
|  84   |   心跳包      |          heartbeat            |     单向     |   number   |       否       |                   数值范围：1                   |
|  85   |  DC输出错误代码    |   DC_Output_error_code   |     只读     |   number   |       否       |       数值范围：0-0xffffffff ,每一位代表一个错误      |
|  86   |  AC输出错误代码    |     AC_Output_error_code      |     只读     |   number   |       否       |      数值范围：0-0xffffffff ,每一位代表一个错误                 |
|  87   |  BMS错误代码    |     BMS_error_code        	  |     只读     |   number   |       否       |       数值范围：0-0xffffffff ,每一位代表一个错误       |
|  88   |     电池总电压    |          Battery_Vol          |     只读     |   number   |       否       |       数值范围：0-0xffffffff,单位:毫伏 mv                   |
|  89   | 单节电池最高电压  |   	  Cell_Max_Vol            |     只读     |   number   |       否       |       数值范围：0-0xffffffff,单位:毫伏 mv          |
|  90   |  单节电池最低电压  |       Cell_Min_Vol            |     只读     |   number   |       否       |       数值范围：0-0xffffffff,单位:毫伏 mv         |
|  91   |   电池循环次数    |         CyclesBack           |     只读     |   number   |       否       |        数值范围：0-65535                |



