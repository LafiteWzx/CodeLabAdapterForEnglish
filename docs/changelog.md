# changelog
*  2018.5.26  v0.1.0
*  2018.5.28  v0.1.1
    *  fix extension_cozmo bug
*  2018.10.24 v0.2.0，[重构笔记](https://wwj718.github.io/scratch3-adapter-refactoring-note.html)
*  2018.11.30 v0.2.3
*  2018.12.03 0.3.0 支持eim_script
*  2018.12.14 0.3.1 fix bug：多个 ws 通道重复 pub；直接展示插件
*  2019.01.16 0.4.0
    *  支持第三方网站接入
    *  增加插件
    *  完善插件的管理，退出后自动清理子进程
    *  第三方库支持
        *  requests
        *  pyserial
        *  Pillow
*  2019.01.29 0.5.0
    *  修复 read 阻塞问题（导致需要额外的一条消息才能推出插件）
    *  支持前端启停插件
    *  将消息用作内部管理机制
    *  rename scratch3-adapter to codelab-adapter
    *  添加树莓派插件（gpiozero）
    *  支撑多个 client 并行作为 UI（同步）
*  2019.01.30 0.5.1
    *  添加调试（Debug）页面
*  2019.02.14 0.6.0 
    *  添加 REST API
    *  统一消息体命名规范：message.data/message.message -> message.payload
    *  添加`打开本地文件目录`功能
    *  内置微信插件（extension_wechat）
    *  添加 typing 库
    *  完善 cli mode
*  2019.02.14 0.6.1
    *  提高微信插件（extension_wechat）的易用性（内置）
*  2019.02.15 0.6.2
    *  fix bug
*  2019.02.16 0.7.0
    *  允许跨域访问 websocket/REST API, 方便开发者调试
    *  为 webdebug 添加 REST API 调试工具
*  2019.02.23 0.7.1
    *  让 Cozmo/Vector 插件支持同步模式（通过添加 messageID），至于采用同步模式还是异步模式，由 client 决定
    *  添加 [extension_mpfshell](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extension_mpfshell.py) 扩展（by [junhuanchen](https://github.com/junhuanchen)）
*  2019.02.26 0.8.0
    *  允许用户添加自定义配置：`~/codelab_adapter/user_settings.py`
        *  典型的配置包括：`cli_load_extension_threads = ["extension_iot"]` 命令行模式（./codelab-adapter --mode cli）默认启动插件
    *  add [gpiozero](https://github.com/RPi-Distro/python-gpiozero) for raspberrypi platform
    *  内置 mqtt client/broker：[hbmqtt](https://hbmqtt.readthedocs.io/en/latest/)
    *  内置 [extension_iot](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extension_iot.py)
    *  更新 extension_mpfshell
*  2019.03.16 0.8.1
    *  微信插件支持收发群消息
    *  添加 web 日志页面
    *  添加重构之后的 blender 插件
*  2019.08.28 2.3.1
*  2019.09.10 2.5.0
    *  安全性改进
*  2019.09.23 2.5.1
    *  使用 Scratch 配色风格的 Web UI
    *  版本号更新提醒（只提醒旧版本，不提醒测试版升级）
    *  报告 adapter core 信息（version）
*  2019.09.23 2.5.3
    *  将 GUI menu 迁移到 Web UI
*  2019.11.13 2.6.0
    *  2.6.x 专注于提高健壮性
    *  添加 rate limit 机制：TokenBucket
    *  为 usb_microbit 添加 TokenBucket
    *  提升 token 安全性（每次启动随机生成；也允许用户在配置文件里固化token）
    *  添加 token 复制按钮（用于粘贴到外部网站） 
    *  将 token 添加到 scratch 启动 url 里（提高安全性）
*  2019.11.13 2.6.1
    *  Scratch3Lab -> CodeLabClub
*  2019.11.13 2.6.2
    *  支持 headless 模式（linux），用于开机自启、无人值守的环境
*  2020.04.17 3.0.0
    *  [发行说明](https://www-old.codelab.club/blog/3-release/)
*  2020.04.30 3.1.0
    *  自动更新 adapter home 目录
    *  插件市场支持extension/node下载(统称为plugin)，node可以是任何有效的url链接
    *  Cozmo 插件支持 event、sensor
    *  Adapter 默认随最后一个client关闭而关闭，允许用户配置该行为
    *  重构 WebUI 的 Adatper socketio client，使其易于二次开发

---

*  2020.12.28 [4.0.0](http://118.31.62.99:10000/blog/2020/12/28/adapter-4)
    *  提供 Linda 支持！
    *  支持激光雷达，将普通地面变为交互式 Scratch 舞台（社区版暂未提供相关支持，目前近提供给CodeLab合作方）
    *  与CodeLab IP访问方式兼容
    *  修复与 token 有关的安全风险
    *  webui, 基于最新codelab_adapter_base.js
    *  解决websocket input token潜在风险
*  2020.12.31 4.1.0
    *  修复目录字符问题（空格、中文）
    *  WebUI 支持 Linda 可视化
    *  修复4.0.0引起的魔杖问题
*  2021.01.20 4.2.0([发布日志](https://www.codelab.club/blog/2021/01/23/4.2-release))
    *  支持新设备
        *  [BrainCo](https://adapter.codelab.club/extension_guide/brainCo/)
        *  [LEGO Mario](https://adapter.codelab.club/extension_guide/legomario/)
        *  [Sphero RVR](https://adapter.codelab.club/extension_guide/spheroRVR/)
    *  新插件
        *  [Sugar](https://adapter.codelab.club/extension_guide/sugar/)
    *  改进Cozmo、Tello、Robomaster插件，使其支持在Scratch中扫描/连接
    *  AdapterThing 目前被视为在Adapter里接入硬件设备的最佳实践
    *  解决webui缩放时，页面失调问题
    *  支持云端更新配置(`global_settings.toml`)
    *  提供node版本服务（静态分析），允许client自动检测node版本
    *  统一所有url中的adapter_token参数
    *  为microbit固件刷入添加ui反馈
    *  重构settings（基于dynaconf），使其简单、灵活、统一，更好地支持环境变量
    *  使得python插件可以向scratch传递json（数据结构）
*  2021.01.23 4.2.1
    *  修复 BrainCo 在windows下的 bug
    *  修复 马里奥 在windows10下的发现问题
    *  支持马里奥掉线通知（UI同步）
    *  使usb microbit、microbit radio插件支持v1/v2版本的micro:bit
    *  修复 windows下 dynaconf 引起的路径错误问题(与`python -m`启动方式有关)
*  2021.01.27 4.2.2
    *  简化microbit相关插件的源码(Adapter Thing风格)
    *  更新micro:bit radio固件到v0.5
    *  为micro:bit radio插件消息添加message_type属性，允许其与避免与控制消息分离
    *  Adapter Client更新到 4.1.2
    *  更新扩展里的通知（统一使用中文）
    *  Client 连接提醒提升到20个
*  2021.02.03 4.2.3
    *  升级Cozmo插件到 `2.1.0` : 提升cozmo启停的健壮性; 添加易用的utils; 添加断线提醒
    *  添加 nodes 进程查看功能(`环境`中提供入口)
    *  [提供设备连接检测脚本(jupyterlab notebook)](https://adapter.codelab.club/user_guide/FAQ/#_9)
    *  提供websocket风格的插件版本检测服务
*  2021.02.06 4.3.0
    *  支持[在 jupyterlab 中使用 pip 安装第三方库](https://adapter.codelab.club/extension_guide/jupyterlab/#_2)！
    *  codelab_adapter_client 升级到 4.1.3: 使得send_message、run_monitor更为直观(服务于交互计算课程)
    *  升级Python kernel插件: 避免传递复杂数据结构，只传递消息(字符串)
    *  添加 overdrive 插件
    *  try bleak, 当某些windows导入bleak失败给出提示，而不是安静失败
    *  升级 RoboMasterEP 到 2.0.1: 添加 已连接提醒、连接失败提醒
*  2021.02.25 4.4.0([发布日志](https://www.codelab.club/blog/2021/02/25/4.4-release))
    *  jupyterlab 升级到最新的 3.X 版本
    *  提供对 PRO_KEY 的支持
        *  使用 PRO_KEY 可以启用 Adapter 的高级特性: 激光雷达、overdrive
    *  提供 microbit 固件烧录 ws api
    *  内置 microbit more 固件
    *  修复 windows 下无法发现 overdrive 的问题
    *  支持连接2台 overdrive
*  2021.03.08 4.4.1
    *  递归复制notebooks/nodes/extensions 目录（初始化），方便用户再分发 Adapter
        *  北京王府国际学校在使用的 `codelab-adapter-4_4_1-AI-alpha` 基于这个机制
    *  codelab_adapter_client 4.1.3 -> 4.1.4: 添加 open_path 函数
        *  `from codelab_adapter_client.utils import open_path`
    *  update microbitMore hex(0.2.0)
    *  overdrive 插件: 添加light2、uTurn、从通知数据中解析更多属性字段(学习CSP项目)、添加电量通知和IntersectionUpdate(十字路口)
    *  usb_microbit: 为 send command 加上锁,避免并行发送串口消息(merge from 刘老师)
*  2021.03.11 [4.5.0](https://www.codelab.club/blog/2021/03/15/4.5-release)
    *  改进 Nodes 扩展的运行机制
        *  full version 使用 multiprocessing 代替 subprocess
        *  提升健壮性(确保node进程在adapter退出后结束)，避免硬件端口被未关闭node占用
    *  所有的 node 支持多进程启动方式
    *  cozmo 内置 3dviewer 依赖(OpenGL)
        *  内置 cozmo cli notebook demo，不支持交互式探索
        *  内置 cozmo cli.py(src), 支持交互式探索
    *  添加 正在运行的nodes UI入口
    *  处理windows以多进程启动node_status_bar_win插件的locale问题
*  2021.03.29 [4.6.0](https://www.codelab.club/blog/2021/03/29/4.6-release)
    *  升级软件/重置主目录时，自动迁移用户数据(`~/codelab_adapter/`)
        *  旧的主目录（`~/codelab_adapter/`）将自动备份，形如: `codelab_adapter_2021-03-29__14-49-04_219298/`, 后缀的数字是时间信息
        *  notebooks/extensions/nodes 里的自定义子目录和文件将自动迁移
        *  user_settings.toml里的自定义信息将自动迁移
    *  尝试提供user_settings web editor接口(alpha)
    *  更新Adapter ssl证书(2022-03-29)
    *  添加证书过期时间配置项
    *  webUI
        *  更新扩展 重命名为 **重置主目录** ，置于 **环境** 目录下
        *  添加正在运行的nodes UI， 置于 **环境** 目录下
    *  codelab_adapter_client -> 4.1.8
        *  添加 send_message, receive_message api (`from codelab_adapter_client.message import send_message, receive_message`)
        *  receive_message 采用非阻塞风格
        *  避免 send_message 过快发送消息
        *  优化 receive_message 循环烧CPU（初学者友好）
    *  overdrive、Lego mario 支持 ble实时 扫描，避免用户长时间等待
    *  修复overdrive连接后的头5s消息阻塞问题
    *  修复 悟空机器人 插件启动超时的bug
    *  弃用 app_settings.py
*  2021.04.09 [4.7](https://www.codelab.club/blog/2021/04/09/4.7-release)
    *  支持增量更新(数据也放在codelab-adpater-client package中), package 地址可配置
        *  webUI 提供更新按钮(`环境 > 增量更新软件包`)
    *  codelab_adapter_client 升级到 4.2.3
        *  递归包含数据(nodes/extensions/notebooks/src), 为日后增量更新准备
        *  message node 不响应 no wait eim积木(服务 交互计算 课程)
    *  修复 Linda bug
        *  修复 linda rd 无法同时读取的 bug
        *  修复Python 中 linda取消后，后台依然挂载的问题(临时方案)
    *  减小软件包的大小，减少下载和解压缩时间
        *  移除所有pyc缓存目录（减小30%-50%的文件量）
        *  windows不内置OpenGL(3000+文件，影响解压时间)
    *  修复蓝牙更新机制（每次扫描5秒）
*  2021.04.09 4.7.1
    *  使用 [CodeLab 社区创作平台](https://create.codelab.club/projects/editor/) 替代 [scratch beta](https://scratch-beta.codelab.club/)
*  2021.04.13 4.7.2
    *  提升二次分发的稳定性，避免一些意外情况
*  2021.04.13 4.7.3
    *  为 microbit radio 插件加上锁
    *  为 Python 插件引入requests
    *  添加可扩展的 webUI ext
*  2021.05.07 4.8.0
    *  webUI 添加打开host目录功能
    *  加速osc send的速度(从scratch出发的消息，延迟在2-3毫秒)
    *  使软件更新源(`LATEST_VERSION`)可配置
    *  添加Toio和microbit Python驱动; 添加 hello_Toio.ipynb hello_microbit.ipynb
    *  添加打开主目录菜单按钮
*  2021.05.19 4.8.1
    *  修复motion senser bug
    *  内置python-aiml（交互计算课程）
*  2021.05.25 4.8.2
    *  添加可编程舞台驱动
    *  内置 programmable_stage.ipynb
    *  修复全局配置文件潜在的预加载bug
*  2021.05.31 4.9.0
    *  使悟空支持 IP 连接
    *  内置 CodeLab 交互计算课程
*  2021.06.18 4.9.1
    *  移除未使用的扩展
    *  使用 adapter token 打开 jupyterlab，允许用户手动打开jupyterlab（可用于应对中文用户名bug）
    *  添加基于ip的悟空机器人连接检测（notebook）
    *  内置 pycozmo
    *  可编程舞台：连接成功后返回ok而不是None
*  2021.08.09 4.9.2
    *  修复 adapter 在windows下升级bug（无法清理干净旧的用户数据）， 同时提供手动清理脚本: `remove-adapter-config-data.bat`
    *  支持家庭版悟空机器人(MINI)
    *  jupyterlab 支持[实时协作](https://adapter.codelab.club/extension_guide/jupyterlab/#_7)和[断点调试](https://jupyterlab.readthedocs.io/en/stable/user/debugger.html)
    *  升级microbit more固件，更加稳定，支持指南针
*  2021.08.17 4.9.21
    *  修复 minecraft 插件的bug
    *  添加 minecraft 相关 notebook: 在 minecraft 控制 turtle
    *  添加 tools notebook: 安装第三方库的脚本
*  2021.09.01 4.9.3
    *  添加 「Python入门基础」 课程（使用git动态更新）
    *  添加 jupyterlab-git支持，需要[本地装有 Git](https://www.codelab.club/blog/2020/08/20/tools/#git)
    *  修复 jupyterlab 多次启动的 bug
*  2021.09.13 4.9.4
    *  发布 windows10 64bit
    *  可以安装tensorflow、mediapipe等大型库
        *  如果一次装不上，则: `import pip;pip.main(['install', 'tensorflow', '--user'])`， 之后 `import pip;pip.main(['install', 'tensorflow'])`
    *  支持 LedBag（参考内置的 notebook）
    *  内置课堂小工具 notebook，诸如计时器和joy-con翻页笔
    *  内置 Snake(类似turtle) notebook
*  2021.09.13 4.9.41
    *  改进可编程书包驱动
        *  支持emoji、中文字体
        *  增加 get_pixel 、save 等功能
        *  支持函数风格(避免引入太多新概念)
        *  支持在 jupyterlab 中动态模拟
        *  引入更多颜色(与imagiCharm保持一致)
        *  添加教学相关例子
        *  等待蓝牙回复确认
    *  更新window microbit hex文件
*  2021.09.22 4.9.5
    *  简化adapter_home迁移机制， 将 adapter_home 内置在软件包里(与全局无关)，避免升级相关问题（windows）
    *  移除jupyterlab-git, 移除 Python入门基础课程(避免.git引起的windows更新问题)
    *  移除增量更新机制
    *  升级codelab_adapter_client -> 4.4.2
    *  改进可编程书包驱动
        *  改进模拟器, 支持交互式查看pixel
        *  入门模式支持 `display_emoji`
        *  使 api 精简清晰(`from codelab_adapter.led_bag import *`); 
        *  修复 clear bug
*  2021.09.29 4.9.51
    *  改进可编程书包驱动
        *  添加动画支持: Animation
            *  添加 Animation 用例(`hello_LedBag.ipynb`)
            *  支持创建、加载、保存动图(gif)
            *  支持把动图同步到可编程led设备(书包、相框等)
    *  添加可编程小火车驱动和notebook(`train_lab.ipynb`)
    *  升级ble驱动(0.12.1)
    *  升级sphero驱动(0.10.1)
*  2021.10.29 4.9.6
    *  支持turtle！
        *  添加 notebook(`hello_turtle.ipynb`)
    *  改进可编程书包驱动
        *  添加函数注释文档
    *  改进 yeelight 支持 
*  2022.03.14 4.9.7
    *  更新 https 证书
    *  移除 JupyterLab 中文包(出于稳定性考虑)