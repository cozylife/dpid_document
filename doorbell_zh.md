### 可视门铃类功能点定义

| DPID |             功能点             |           标识符           | 数据传输类型 |  功能点类型  | 是否支持自动化 |                          功能点属性                          |
| :--: | :----------------------------: | :------------------------: | :----------: | :----------: | :------------: | :----------------------------------------------------------: |
|  1   |              开关              |           switch           |     双向     |    number    |       是       | 数值范围：00~FF，转化为二进制为1111 1111<br/>其中每一位代表一路开关，最多支持8路开关同时设置 |
|  2   |          开关1倒计时           |        countdown_1         |     双向     |    number    |       否       |                                                              |
|  4   |         移动检测灵敏度         |        motion_sens         |     双向     |     enum     |       否       |                     1：低，2：中，3：高                      |
|  5   |        移动检测触发频率        |      motion_interval       |     双向     |    number    |       否       |                 两次移动检测触发最小时间间隔                 |
|  6   |          传输视频模式          |        video_format        |  单向，上报  |     enum     |       否       |                      1：MJPEG_RAW，2：H264_RAW, 3:H264_WEBRTC                       |
|  7   |          传输音频格式          |        audio_format        |  单向，上报  |     enum     |       否       |             1：PCM，2：a-law，3：μ-law，4：Opus              |
| 101  |          设备发起呼叫          |    device_request_call     |  单向，上报  |    number    |       否       |        1：设备处于呼叫状态，2：设备不在呼叫状态，弃用        |
| 102  |              电量              |        electricity         |  单向，上报  |    number    |       是       |            取值范围0-1000，步进为1, 单位：千分比             |
| 103  |           低电量报警           |      low_power_alert       |     单向     |    number    |       是       |                 1：低电量报警；2：不处于报警                 |
| 104  |          红外补光设置          |       ir_fill_light        |  单向，下发  |    number    |       否       |                  1：设置补光；2：不设置补光                  |
| 105  |            移动检测            |    motion_detect_enable    |  单向，下发  |    number    |       否       |                   1：开启检测；2：关闭检测                   |
| 106  |          移动检测报警          |    motion_detect_alert     |  单向，上报  |    number    |       是       |                    1：报警；2：不处于报警                    |
| 107  |       设备发起呼叫的原因       | device_request_call_reason |  单向，上报  |    number    |       否       |                枚举值，1：按键；2：检测到移动                |
| 108  |          移动检测行为          |    motion_detect_action    |  单向，下发  |    number    |       否       | 枚举值；1：不做任何处理；2：拍图；3：呼叫用户；4：拍图并且呼叫用户 |
| 109  |        用户是否应答呼叫        |        user_answer         |  单向，下发  |    number    |       否       |                  枚举值，1：接听；2：不接听                  |
| 110  |             会话id             |         session_id         |  双向，上报  | string 4byte |       否       | 该值由设备端、app端生成作为一次通话的随机id。设备端在查询返回时，若该值为空表示设备没有通话中； |
| 111  | 用户要求设备推送视频流、音频流 |         user_call          |  单向，下发  |    number    |       否       | 用户主动发起呼叫，需要和session id一起工作。1：用户要求；0：用户取消要求 |
| 112  |            通讯类型            |         call_type          |     双向     |    number    |       否       |            枚举值，1：视频；2：音频；3：视频+音频            |
| 113  |    用户关闭session_channel     |     user_close_reason      |  单向，下发  |    number    |       否       | 枚举值，0：没有原因，表示不在通话中；1：用户关闭；2：超时关闭 |
| 114  |        设备关闭session         |    device_close_reason     |  单向，上报  |    number    |       否       | 枚举值，，0：没有原因，表示不在通话中；1：用户没有接听；2：超时关闭 |
| 115  |           视频分辨率           |      video_resolution      |     双向     |    number    |       否       |                    枚举值，1:720， 2:480                     |
| 116  |            视频帧率            |         video_fps          |     双向     |    number    |       否       |                    取值范围1-30，步进为1                     |
| 117  |      设备端推送类型的枚举      |         push_type          |  单向，下发  |    number    |       否       |  枚举类型；1：内网通信；2：公网通信；3：内网通信和公网通信   |
| 118  |     使用的协议版本（暂无）     |                            |              |              |                |                                                              |
| 119  |        设备是否应答呼叫        |       device_answer        |  单向、上报  |    number    |       否       |                  枚举值，1：接听；2：不接听                  |
| 120  |        进入深度睡眠时间        |      enter_sleep_time      |     双向     |    number    |       否       |  数值范围：0-1440, 0：关闭主动呼叫，60：一小时  1440：永久   |
| 121  |        设备信号源1图像旋转角度        |   device_image_rotation    |     双向     |    number    |       否       |        枚举值，0：0度，1：90度，2：180度，3：270度，         |
| 122  |        用户信号源1图像旋转角度        |    user_image_rotation     |     双向     |    number    |       否       |        枚举值，0：0度，1：90度，2：180度，3：270度，         |
| 123  |          视频分辨率宽          |   video_resolution_width   |     双向     |    number    |       否       |                      数值范围，320-1920                      |
| 124  |          视频分辨率高          |   video_resolution_high    |     双向     |    number    |       否       |                      数值范围，320-1920                      |
| 125  |            channel             |           token            |     双向     |    string    |       否       |                   表示设备当前通话的token                    |
| 126  |     设备播放音频的channel      |    device_audio_channel    |     双向     |    string    |       否       | 设备播放音频的channel，如果设备当前有播放，有人申请播放会返回当前正在播放的channel |
| 127  |          当前通话列表          |         token_list         |  单向，下发  |    string    |       否       |          当前通话列表，例如 ["token1", "token2"]          |
| 128  |             信号源             |       signal_source        |     双向     |    number    |       否       |    设备音视频信号源，如两个摄像头可通过这个切换，默认为0     |
| 129  |        设备信号源2图像旋转角度        |   device_image_rotation    |     双向     |    number    |       否       |        枚举值，0：0度，1：90度，2：180度，3：270度，         |
| 130  |        用户信号源2图像旋转角度        |    user_image_rotation     |     双向     |    number    |       否       |        枚举值，0：0度，1：90度，2：180度，3：270度，         |
