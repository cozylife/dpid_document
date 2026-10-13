### Small Appliance DPID Definition

| DPID  |          Function          |        Identifier        | Data Transfer Type | Data Type | Support Automation | Function Attributes |
| :---: | :------------------------: | :----------------------: | :----------------: | :-------: | :----------------: | ------------------- |
|   1   |           Switch           |       switch_power       |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|   2   |            Mode            |           mode           |    Bidirectional   |   enum    |         No         | Value range: 0-3; 0: heating; 1: keep warm; 2: cooling; 3: sterilizing |
|   3   |       Water volume         |        water_vol         |    Bidirectional   |   enum    |         No         | Value range: 0-2; 0: small cup; 1: medium cup; 2: large cup |
|   4   |       Water outlet         |        water_way         |    Bidirectional   |   enum    |         No         | Value range: 0-3; 0: left outlet; 1: middle outlet; 2: start dispensing; 3: stop dispensing |
|   5   |     Dispensing temperature |        water_temp        |    Bidirectional   |   enum    |         No         | Value range: 0-3; 0: cold water; 1: hot water; 2: warm water; 3: ice water |
|   6   |      Dispensing type       |       water_class        |    Bidirectional   |   enum    |         No         | Value range: 0-7; 0: flower tea; 1: fruit tea; 2: black tea; 3: green tea; 4: coffee; 5: milk powder; 6: instant noodles; 7: lemonade |
|   7   |   Temperature setting      |        temp_set          |    Bidirectional   |  number   |         No         | Value range: 0-100 |
|   8   |   Temperature reading      |        temp_get          |       One-way      |  number   |         No         | Value range: 0-100 |
|   9   |           Voice            |        sound_vol         |    Bidirectional   |  number   |         No         | Value range: 1-10, AI voice volume |
|  10   |        Error code          |       error_code         |      Read-only     |   enum    |         No         | Value range: 0-10; 0: E1, 1: E2, 2: E3, 3: E4 |
|  11   |          Heating           |         heating          |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: heating state, 1: not heating |
|  12   |       Keep warm            |    heat_preservation     |    Bidirectional   |   enum    |         No         | Value range: 0-24; 0: keep-warm state, non-0: not keep-warm |
|  13   |          Cooling           |           cool           |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: cooling state, 1: not cooling |
|  14   |     Left water outlet      |     left_water_way       |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: dispensing from the left; 1: not dispensing from the left |
|  15   |     Right water outlet     |     right_water_way      |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: dispensing from the right; 1: not dispensing from the right |
|  16   |   Dispensing time reading  |    water_times_get       |      Read-only     |  number   |         No         | 0-50 |
|  17   |  Left dispensing time      |  left_water_times_set    |    Bidirectional   |  number   |         No         | 0-50 |
|  18   |  Right dispensing time     |  right_water_times_set   |    Bidirectional   |  number   |         No         | 0-50 |
|  19   |    Boiling point setting   |    boiling_temp_set      |    Bidirectional   |  number   |         No         | 80-100 |
|  20   |   Keep-warm time setting   |     heat_times_set       |    Bidirectional   |  number   |         No         | 1-24 |
|  21   |      Heating level         |        heat_gear         |    Bidirectional   |  number   |         No         | Value range: 1 to 3; 1: level 1; 2: level 2; 3: level 3 |
|  22   |     Vibration level        |     vibration_gear       |    Bidirectional   |  number   |         No         | Value range: 1 to 3; 1: level 1; 2: level 2; 3: level 3 |
|  23   |  Heating percentage        |    heat_percentage       |      Read-only     |  number   |         No         | Value range: 1 to 100, step 1 |
|  24   |      Water temperature     |        water_temp        |    Bidirectional   |  number   |         No         | Value range: 0-1000, step 1. 0 means invalid; 1 means 0.1℃, 10 means 1℃ |
|  25   |       Seat temperature     |        sit_temp          |    Bidirectional   |  number   |         No         | Value range: 0-1000, step 1. 0 means invalid; 1 means 0.1℃, 10 means 1℃ |
|  26   |  Wind temperature level    |     wind_temp_level      |    Bidirectional   |   enum    |         No         | 1 means lv1; 2 means lv2; 3 means lv3; 4 means lv4 |
|  27   |     Smart temperature      | intelligent_temperature  |    Bidirectional   |   enum    |         No         | 0 means invalid; 1 means spring/autumn; 2 means summer; 4 means winter |
|  28   |      Function mode         |      function_mode       |    Bidirectional   |   enum    |         No         | 0: stop, 1: flip lid, 2: flush, 3: flip seat ring, 4: bubble guard, 5: dry, 6: self-clean, 7: rear wash, 8: child wash, 9: feminine wash, 10: energy saving, 11: night mode, 12: lighting |
|  29   |    Wash water pressure     |   wash_adjust_pressure   |    Bidirectional   |   enum    |         No         | 1: level 1; 2: level 2; 3: level 3; 4: level 4 |
|  30   |      Wash position         |   wash_adjust_position   |    Bidirectional   |   enum    |         No         | 1: level 1; 2: level 2; 3: level 3; 4: level 4 |
|  31   |      Moving wash           |     wash_adjust_move     |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  32   |     Sitz bath wash         |     wash_adjust_bath     |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  33   |     Hot-cold massage       |     wash_adjust_temp     |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  34   |    Strong-weak massage     |    wash_adjust_strong    |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  35   |  Auto connect nearby devs  |       auto_connect       |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  36   |   Simulate human seating   |     simulated_human      |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  37   |  Start bubble on seating   |       start_bubble       |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  38   |     UV sterilization       |      uv_disinfect        |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  39   |       Voice system         |       voice_mode         |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  40   |        Flush mode          |       flush_mode         |    Bidirectional   |   enum    |         No         | 0: flush before drying; 1: flush after leaving the seat |
|  41   |   Radar sensing distance   |        radar_dis         |    Bidirectional   |   enum    |         No         | 1: level 1; 2: level 2; 3: level 3; 4: level 4; 5: level 5 |
|  42   |  Auto close lid time       |   auto_close_second      |    Bidirectional   |  number   |         No         | Value range: 0-7200; step 1; 1 means 1 second; 60 means 1 minute |
|  43   |  Water tank fill time      |    water_tank_second     |    Bidirectional   |  number   |         No         | Value range: 0-7200; step 1; 1 means 1 second; 60 means 1 minute |
|  44   |  Single wash duration      |   singe_clean_second     |    Bidirectional   |  number   |         No         | Value range: 0-7200; step 1; 1 means 1 second; 60 means 1 minute |
|  45   |   Restore default settings |          reset           |       One-way      |   enum    |         No         | Only value 1 is valid; 1 means the device restores default settings |
|  46   |        Auto flush          |        auto_flush        |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  47   |   Bowl pre-wetting on seating  |        seat_open         |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  48   |      Smart lid flip        |       smart_flip         |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  49   |       Foot sensing         |      foot_induction      |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  50   |        Timer switch        |   timing_switch_power    |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  51   |      Vibration switch      |   shock_switch_power     |    Bidirectional   |   enum    |         No         | 0: off; 1: on |
|  52   |        Screen off          |       screen_down        |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  53   |        Child lock          |       child_lock         |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  54   |          Wash              |          wash            |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  55   |        Night light         |       night_light        |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  56   |          Mute              |          mute            |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  57   |      Timed power on        |       timed_start        |    Bidirectional   |   enum    |         No         | Value range: 1-24; send 0 to cancel |
|  58   |      Timed power off       |        timed_off         |    Bidirectional   |   enum    |         No         | Value range: 1-12; send 0 to cancel |
|  59   |       Power button         |      power_button        |       One-way      |   enum    |         No         | Value range: 1; always send 1; transmission direction to be confirmed |
|  60   |  Water-heating blanket mode |        snt_mode         |    Bidirectional   |   enum    |         No         | Value range: 0-3; 0: water heating, 1: preheat, 2: comfortable sleep, 3: mite removal |
|  61   | Water-heating blanket error |     snt_error_code      |      Read-only     |   enum    |         No         | Value range: 0-5; 0: normal, 1: water shortage please add water, 2: sensor fault, 3: over-temperature fault, 4: product tipped over, 5: anti-freeze on |
|  62   |       Heater mode          |        qnq_mode          |    Bidirectional   |  number   |         No         | Value range: 0-2; 0: cold air, 1: low heat, 2: high heat |
|  63   |       Oscillation          |         shake            |    Bidirectional   |   enum    |         No         | Value range: 0-1 |
|  64   |     Air purification       |    air_purification      |    Bidirectional   |   enum    |         No         | Value range: 0-1 |
|  65   |   Constant temperature     |  constant_temperature    |    Bidirectional   |   enum    |         No         | Value range: 0-1 |
|  66   |      Energy saving         |   energy_conservation    |    Bidirectional   |   enum    |         No         | Value range: 0-1 |
|  67   |       Heat quantity        |      heat_quantity       |       One-way      |   enum    |         No         | Value range: 0-1; 0: decrease, 1: increase |
|  68   |          Lift              |          lift            |       One-way      |   enum    |         No         | Value range: 0-2; up / stop / down |
|  69   |         Drying             |         drying           |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  70   |        Air dry             |        air_dry           |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  71   |        Disinfect           |       disinfect          |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  72   |       Illumination         |      illumination        |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  72   |       Illumination         |      illumination        |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  73   |          Bath              |          bath            |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  74   |          Blow              |          blow            |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  75   |        Ventilate           |       ventilate          |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  76   |      Strong warmth         |      strongWarmth        |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  77   |       Weak warmth          |       weakWarmth         |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  78   |    Oscillation switch      |       auto_switch        |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  79   |  Overheat protection alert |     overheat_switch      |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  80   |  Tip-over protection alert |     tipping_switch       |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  81   |        Countdown           |        countdown         |    Bidirectional   |  number   |         No         | Value range: 0-86400, unit: s |
|  82   |   Temperature unit (℃/℉)   |    battery_temp_unit     |    Bidirectional   |  number   |         No         | Value range: 0-1; 0: ℃, 1: ℉ |
|  83   | 24h auto shutdown alert    |    auto_shutdown_tips    |    Bidirectional   |   enum    |         No         | Value range: 0-1; 0: off, 1: on |
|  84   |       Current humidity     |     humidity_report      | One-way, report only |   int   |         No         | Value range: 0-99, unit: percent |
