### Energy Storage Battery DPID Definition

| DPID  |             Function              |           Identifier            | Data Transfer Type | Data Type | Support Automation |                  Function Attributes                   |
| :---: | :-------------------------------: | :-----------------------------: | :----------------: | :-------: | :----------------: | :----------------------------------------------------: |
|   1   |              Switch               |          switch_power           |    Bidirectional   |  number   |         No         | Value range: 0000-FFFF, binary 1111 1111 1111 1111, each bit represents one channel, up to 16 channels can be set at the same time |
|   2   |      Current status of battery    |         current_status          |      Read-only     |  number   |         No         |        Enum: 0 powered off, 1 charging, 2 discharging   |
|   3   |         Battery level             |            battery              |      Read-only     |  number   |         No         |            Value range: 0-100, unit: %                  |
|   4   |         Total output power        |          total_output           |      Read-only     |  number   |         No         |      Value range: 0-3000 (TBD), unit: W     |
| 5-20  |       Branch output power         |          output1-16             |      Read-only     |  number   |         No         |      Value range: 0-3000 (TBD), unit: W     |
|  21   |         Total input power         |         total_intput            |      Read-only     |  number   |         No         |      Value range: 0-3000 (TBD), unit: W     |
| 22-29 |        Branch input power         |          intput1-8              |      Read-only     |  number   |         No         |      Value range: 0-3000 (TBD), unit: W     |
|  30   |      Remaining usable time        |    residue_available_time       |      Read-only     |  number   |         No         |           Value range: 0-65535, unit: min               |
|  31   |      Remaining charging time      |    residue_charging_time        |      Read-only     |  number   |         No         |           Value range: 0-65535, unit: min               |
|  32   |      Battery temperature (K)      |          battery_temp           |      Read-only     |  number   |         No         | Value range: 0-500, unit: K, e.g. 303 K means 30℃ |
|  33   |       Floodlight mode             |        floodlight_mode          |    Bidirectional   |  number   |         No         |                        Enum                             |
|  34   |     Floodlight brightness         |         floodlight_v            |    Bidirectional   |  number   |         No         |               Value range: 1-1000                       |
|  35   |           LED mode                |            led_mode             |    Bidirectional   |  number   |         No         |                        Enum                             |
|  36   |           LED hue                 |             led_h               |    Bidirectional   |  number   |         No         |            Value range: 0-360 or FFFF                   |
|  37   |         LED saturation            |             led_s               |    Bidirectional   |  number   |         No         |            Value range: 0-1000 or FFFF                  |
|  38   |        LED color temperature      |             led_t               |    Bidirectional   |  number   |         No         |            Value range: 0-1000 or FFFF                  |
|  39   |         LED brightness            |             led_v               |    Bidirectional   |  number   |         No         |               Value range: 1-1000                       |
|  40   |         Standby time              |         standby_time            |    Bidirectional   |  number   |         No         |           Value range: 0-1440, unit: min                |
|  41   |       Screen-off time             |        led_down_time            |    Bidirectional   |  number   |         No         |           Value range: 0-65535, unit: s                 |
|  42   |          Prompt tone              |            prompt               |    Bidirectional   |  number   |         No         |                0 off, 1 on                              |
|  43   |         Key tone                  |           key_sound             |    Bidirectional   |  number   |         No         |                0 off, 1 on                              |
|  44   |          Fault code               |          Fault code             |      Read-only     |  number   |         No         |              Value range: 0-FF                          |
|  45   |         E-Turbo state             |         E_Turbo_state           |    Bidirectional   |  number   |         No         |            0 disabled, 1 enabled                        |
|  46   |      Preferred charge mode        |     Preferred_charge_mode       |    Bidirectional   |  number   |         No         |   0 charge simultaneously, 1 slave priority, 2 master priority |
|  47   |        AC fast charge power       |       AC_fastinput_power        |    Bidirectional   |  number   |         No         |       Value range: 0-5000, resolution: 1 W              |
|  48   |        AC slow charge power       |       AC_slowinput_power        |    Bidirectional   |  number   |         No         |       Value range: 0-5000, resolution: 1 W              |
|  49   |        AC standby time            |        AC_standby_time          |    Bidirectional   |  number   |         No         |           Value range: 0-1440, unit: min                |
|  50   |     Restore factory parameters    |       Restore_parameters        |    Bidirectional   |  number   |         No         | 0 keep current parameters, 1 restore factory parameters |
|  51   |    Number of online battery packs |   Battery_pack_online_num       |      Read-only     |  number   |         No         |                  Range: 0-15                            |
|  52   |      Faulty battery pack number   |    Battery_pack_fault_num       |      Read-only     |  number   |         No         |                  Range: 0-15                            |
|  53   |    Battery pack charge power      |   Battery_pack_input_power      |      Read-only     |  string   |         No         | FFFFFFFF...FFFF: 15 groups of FFFF, 0000-FFFF: 0-65535  |
|  54   |   Battery pack discharge power    |   Battery_pack_output_power     |      Read-only     |  string   |         No         | FFFFFFFF...FFFF: 15 groups of FFFF, 0000-FFFF: 0-65535  |
|  55   |        Battery level              |           batteryWH             |      Read-only     |  number   |         No         | Value range: TBD (actual remaining capacity), unit: WH |
|  56   |      Battery 2 temperature (K)    |     battery_temp2_two           |      Read-only     |  number   |         No         | Value range: 0-500, unit: K, e.g. 303 K means 30℃ |
|  57   |      Temperature unit (℃/℉)       |      battery_temp_unit          |    Bidirectional   |  number   |         No         |        Value range: 0-1; 0: ℃, 1: ℉                     |
|  58   |       Brightness level            |          light_gear             |    Bidirectional   |  number   |         No         |             Value range: 1, 2, 3                        |
|  59   |     LED hue (default scheme)      |        led_h_defaults           |    Bidirectional   |  number   |         No         |              Value range: 0/1                           |
|  60   |        Buzzer switch              |            buzzer               |    Bidirectional   |  number   |         No         |              Value range: 0/1                           |
|  61   |        AC voltage setting         |           ac_voltage            |    Bidirectional   |  number   |         No         | Value range: 0-3. 0: 100V/50Hz or 60Hz, 1: 120V/60Hz, 2: 240V/50Hz, 3: 230V/50Hz |
|  62   |        DC voltage setting         |           dc_voltage            |    Bidirectional   |  number   |         No         |           Value range: 0: 12V/24V                       |
|  63   |       AC output switch            |           ac_switch             |    Bidirectional   |  number   |         No         |              Value range: 0/1                           |
|  64   |    AC output auto sleep           |         ac_output_sleep         |    Bidirectional   |  number   |         No         |              Value range: 0/1                           |
|  65   |   Priority charging selection     | priority_charging_selection     |    Bidirectional   |  number   |         No         |        Value range: 0-2 'AC, DC, MPPT'                  |
|  66   |     AC charging time statistics   |        ac_charge_time           |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  67   |    AC charging energy statistics  |        ac_charge_power          |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  68   |    AC discharge time statistics   |      ac_discharge_time          |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  69   |   AC discharge energy statistics  |      ac_discharge_power         |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  70   |     DC charging time statistics   |        dc_charge_time           |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  71   |    DC charging energy statistics  |        dc_charge_power          |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  72   |    DC discharge time statistics   |      dc_discharge_time          |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  73   |   DC discharge energy statistics  |      dc_discharge_power         |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  74   |    MPPT charging time statistics  |       mppt_charge_time          |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  75   |   MPPT charging energy statistics |      mppt_charge_power          |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  76   |   MPPT discharge time statistics  |     mppt_discharge_time         |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  77   |  MPPT discharge energy statistics |     mppt_discharge_power        |      Read-only     |  number   |         No         |          Value range: (empty)                           |
|  78   |  Battery pack remaining usable time |  Battery_pack_output_time     |      Read-only     |  string   |         No         |           Value range: 0-65535, unit: min               |
|  79   |      Battery pack battery level   | Battery_pack_surplus_power      |      Read-only     |  number   |         No         |            Value range: 0-100, unit: %                  |
|  80   |      Battery pack temperature     |     Battery_pack_temp           |      Read-only     |  number   |         No         |              Value range: 0-500                         |
|  81   |        LED strip hue              |          led_bar_h              |    Bidirectional   |  number   |         No         |              Value range: 0-360                         |
|  82   |     LED strip saturation          |          led_bar_s              |    Bidirectional   |  number   |         No         |            Value range: 0-1000 or FFFF                  |
|  83   |     LED strip brightness          |          led_bar_v              |    Bidirectional   |  number   |         No         |               Value range: 1-1000                       |
|  84   |          Heartbeat                |          heartbeat              |       One-way      |  number   |         No         |              Value range: 1                              |
|  85   |      DC output error code         |     DC_Output_error_code        |      Read-only     |  number   |         No         | Value range: 0-0xffffffff, each bit represents one error |
|  86   |      AC output error code         |     AC_Output_error_code        |      Read-only     |  number   |         No         | Value range: 0-0xffffffff, each bit represents one error |
|  87   |          BMS error code           |        BMS_error_code           |      Read-only     |  number   |         No         | Value range: 0-0xffffffff, each bit represents one error |
|  88   |        Total battery voltage      |         Battery_Vol             |      Read-only     |  number   |         No         |   Value range: 0-0xffffffff, unit: millivolt mv         |
|  89   |      Max single-cell voltage      |        Cell_Max_Vol             |      Read-only     |  number   |         No         |   Value range: 0-0xffffffff, unit: millivolt mv         |
|  90   |      Min single-cell voltage      |        Cell_Min_Vol             |      Read-only     |  number   |         No         |   Value range: 0-0xffffffff, unit: millivolt mv         |
|  91   |        Battery cycle count        |          CyclesBack             |      Read-only     |  number   |         No         |              Value range: 0-65535                       |
