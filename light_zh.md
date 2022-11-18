### 照明类功能点定义
| DPID  |      功能点      |       标识符        | 数据传输类型 | 功能点类型 | 是否支持自动化 | 功能点属性|
| :---: | :--------------: | :-----------------: | :----------: | :--------: | :------------: | :---: |
|   1   |       开关       |     switch_led      |     双向     |    enum    |       是       | 枚举值：0-2 <br> 0：关闭 <br> 1: 打开|
|   2   |       模式       |      work_mode      |     双向     |   enum   |       否       | 枚举值：0-2；<br>0:static,  1:scene, 2:music_out 3:diy, 4:music_inc, 5:2d_text, 6:2d_diy, 7:picture|
|   3   |      冷暖值      |     temp_value      |     双向     |   number   |       否       | 数值范围：0-1000, 65535(0xffff) 代表本数值无效|
|   4   |      亮度值      |    bright_value     |     双向     |   number   |       否       | 数值范围：10-1000|
|   5   |      色度值      |      hue_value      |     双向     |   number   |       否       | 数值范围：0~360, 65535(0xffff) 代表本数值无效|
|   6   |      饱和值      |      sat_value      |     双向     |   number   |       否       | 数值范围：0-1000, 65535(0xffff) 代表本数值无效|
|   7   |       场景       |     scene_data      |     双向     |   string   |       否       | Value: 00HHHHSSSSTTTT; <br>00：情景号;一共16种动态场景，场景固定变换方式（0~3渐变，4~7跳变，8~b呼吸，c~f频闪） <br>单色、双色、三色、七色(需要考虑有些效果单色做不了)<br>H(色度：0-360，FFFF代表只使用T值); <br>S (饱和：0-1000，FFFF代表只使用T值);<br>T(色温值, 0-1000，FFFF代表只使用HS值);<br> 注：HST最多支持7组，所有颜色亮度共用全部亮度值，所有动态模式的速度公用速度值，但倍率可做区分；最多需要1+7*6=43个字节表示 |
|   8   |       速度       |     speed_value     |     双向     |   number   |       否       | 动态场景共用速度，数值范围：10-1000|
|   9   |     断电记忆     |    power_memory     |     双向     |   number   |       否       | 数值范围：0-1|
|  10   |    咪头灵敏度    |  sensitivity_value  |     双向     |   number   |       否       | 数值范围：1-10|
|  11   |     RGB线序      |      rgb_turn       |     双向     |   enum   |       否       | 数值范围：0~5, 默认为0；<br>0：GRB；1：RGB；2：GBR；3：RBG；4：BRG；5：BGR；<br>调整线序时需要通过APP引导用户操作，现在灯亮起的是什么颜色，亮起了多少个灯珠，这样的方式来计算实际使用的灯珠数|
|  12   |     灯珠点数     |     chip_point      |     双向     |   number   |       否       | 幻彩芯片点数，数值范围：10-1000|
|  13   |      倒计时      |      countdown      |     双向     |   number   |       否       | 数值范围：0-86400,单位：s|
|  14   |     周期定时     |    normal_timer     |     双向     |   string   |       否       | 支持本地定时，重启无效|
|  15   |     音乐模式     |     music_index     |     双向     |   enum   |       否       | 数值范围：0~3，对应不同的音乐效果|
|  16   |   幻彩静态颜色   | dream_static_color  |     双向     |   string   |       否       | 用于控制幻彩整段数据&lt;br/&gt;Value:  HHHHSSSSTTTT... &lt;br/&gt;整体控制: HHHHSSSSTTTT仅有一组颜色&lt;br/&gt;分别控制: HHHHSSSSTTTT...需提供30组颜色&lt;br/&gt;H(色度：0-360，FFFF代表只使用T值); &lt;br/&gt;S (饱和：0-1000，FFFF代表只使用T值);&lt;br/&gt;T(色温值, 0-1000，FFFF代表只使用HS值);|
|  17   |   幻彩实时控制   | dream_control_data  |     只写     |   string   |       否       | 用于快速响应幻彩分段控制，设备端仅执行本指令，不做任何回复。&lt;br/&gt;Value:  01HHHHSSSSTTTT&lt;br/&gt;01: 幻彩灯带段落号(范围0~29，当段落号为FF时代表控制整段，此时不能写入存储。)|
|  18   |   幻彩场景内容   |  dream_scene_value  |     双向     |   string   |       否       | 组合不同颜色和不同动画，构成自定义场景&lt;br/&gt;Value: HHHHSSSSTTTT...000102...FFFFSS&lt;br/&gt;HHHHSSSSTTTT... : 固定7组颜色&lt;br/&gt;000102...FFFF：动画列表(00跳动+01渐变+02流星..   共10种，不足补FF)&lt;br/&gt;SS:场景对应的执行速度，取值范围00~64|
|  19   |   幻彩场景编号   |  dream_scene_index  |     双向     |   number   |       否       | 场景ID，0-19为DIY场景，20-255为内置场景，切换场景时仅执行该DPID即可。|
|  20   | 幻彩静态颜色过渡 | dream_static _fade  |     双向     |   enum   |       否       | 0: 关闭渐变；1: 开启渐变|
|  21   |  手机麦采集数据  |      music_fft      |     只写     |   string   |       否       | 无|
|  23   |     剩余电量     |     dump_energy     |     只读     |   number   |       否       | 0~100|
|  24   |     电池电压     |    cell_voltage     |     只读     |   number   |       否       | 0~暂无范围 单位mV|
|  25   |     输入电流     |  incoming_current   |     只读     |   number   |       否       | 0~暂无范围 单位mA|
|  26   |     输出电流     |   current_output    |     只读     |   number   |       否       | 0~暂无范围 单位mA|
|  27   |     设备温度     |     temperature     |     只读     |   number   |       否       | -127C° ~ 1000C°  传入值 0~1127|
|  28   |     充电状态     |   charging_state    |     只读     |   enum   |       否       | 数值范围: 0~2   0:断开 1:充电  2：快充|
|  30   |   内置场景索引   |     scene_index     |     读写     |   enum   |       否       | 枚举类型：1-100|
|  31   | 修改经典蓝牙名称 |   classic_bt_name   |     读写     |   string   |       否       | 0-255字节，使用unicode的utf-8编码|
|  32   |   RGB颜色矫正    |     rgb_adjust      |     读写     |   string   |       否       | 三个值 千分比  长度12    RRRRGGGGBBBB|
|  33   |   灯珠点数详情   |     point_info      |     读写     |   string   |       否       | 三个值 点数+长+宽  长度12    NNNNHHHHWWWW|
|  34   |      信号源      |    signal_source    |     读写     |   number   |       否       | 0~暂无范围|
|  35   | 幻彩点阵变化模式 |      dir_index      |     双向     |   enum   |       否       | 数值范围：0-6;<br> 0：固定； 1：左移； 2：右移； 3：下移； 4：上移； 5：闪烁； 6：呼吸；|
|  36   |  文本字符总数量  |    text_char_num    |     只写     |   number   |       否       | 数值范围：0-10;|
|  37   | 单个文本字符内容 |   text_char_point   |     只写     |   string   |       否       | 组合不同的文本字符显示，Value: 01HHHHSSSSTTTT...|
|  38   | 文本字符变换模式 | text_char_modecolor |     只写     |   string   |       否       | 文本字符的颜色模式，Value: 01HHHHSSSSTTTT; <br>01：颜色模式号;一共6种颜色模式，1：纯色，所有字符共用一种颜色 2~5：字符动态变化色彩|
|  39   | 文本边框底色内容 |  text_border_color  |     只写     |   string   |       否       | 文本边框模式和底色，Value: 00HHHHSSSSTTTT; <br>00:边框模式，0-3；HHHHSSSSTTTT：字符底色，如果为无颜色则，把TTTT设置为0X0000;|
|  40   |    平面diy点     |    diy_2d_point     |     只写     |   string   |       否       | 用于使用平面diy点的显示，不回复，Value: 000000HHHHSSSS0000HHHHSSSS...; <br>00:平面0，首包需在第二高位上置1，最后一包结束需在最高位置1，共有5张 0000:点位 HHHHSSSS:对应每个点位的颜色|
|  41   |   幻彩图像模式   |   pincture_index    |     双向     |   enum   |       否       | 数值范围：0-19|
|  43   |  点阵屏旋转方向    |   screen_dir    |     双向     |   number   |       否       | 数值范围：0-3|