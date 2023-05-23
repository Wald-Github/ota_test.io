# 简介

阿里云的[物联网平台](https://www.aliyun.com/product/iot)提供安全可靠的设备连接通信能力, 帮助用户将海量设备数据采集上云

设备可通过集成 `Link SDK` 具备连接物联网平台服务器的能力, 以及进而使用物联网平台的其它高级能力

---
这个SDK以C99编写, 开源发布, 支持多种操作系统和硬件平台, 阅读本文开始使用, 访问[SDK的线上文档首页](https://code.aliyun.com/linksdk/docs/wikis/home)得到更多信息

# 了解SDK架构

<img src="https://linkkit-export.oss-cn-shanghai.aliyuncs.com/sdk_new_arch.png" width="800">

# 获取SDK内容及用户编程导引

> **SDK基座:** [下载地址](https://code.aliyun.com/linksdk/base/repository/archive.zip?ref=master)

下载SDK基座得到的, 主要含上图中的**SDK核心模块**, 它本身已是完整可用的了, 点击以下链接阅读编程导引开始使用

+ [MQTT连云能力](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/MQTT_Connect)
+ [HTTP连云能力](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/HTTP_Connect)
+ [RRPC](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/RRPC_Process)
+ [在线设备接收广播](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/Broadcast_Process)

---
除此以外, 以上获取的SDK基座上, 还可以由用户选择动态安插, 装备上其它高阶的能力, 点击以下链接阅读编程导引开始使用

+ [Bootstrap(引导服务)](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/Bootstrap_Service)
+ [OTA(固件升级)](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/OTA_Service)
+ [Data-Model(物模型)](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/Data_Model_Process)
+ [Dynreg(动态注册)](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/Dynreg_Service)
+ [NTP(时间同步)](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/NTP_Service)
+ [Shadow(设备影子)](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/Shadow_Service)
+ [Logpost(日志上云)](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/Logpost_Service)
+ [Devinfo(设备标签)](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/Devinfo_Service)

---
在面向应用的编程导引外, 以上所有组件也提供面向代码的详细手册, [SDK的线上手册地址](http://gaic.alicdn.com/ztms/linkkit/html/index.html)

# 装备高阶能力

以上高阶能力, 任意两两之间无依赖关系, 仅依赖SDK核心模块(`core`目录), 用户装备任一种能力的方式都是一致的

+ 下载组件压缩包, 每一种高阶能力对应一个组件代码压缩包
+ 解压组件压缩包, 放置到 `components/xxx` 目录

> 目前已就绪的高阶组件有

| **高阶组件**    | **组件说明**                                | **下载地址**
|:---------------:|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------
| `Bootstrap`     | *实时动态的同步国家与地区的建连信息给设备*  | [Bootstrap组件下载链接](https://code.aliyun.com/linksdk/linksdk-bootstrap/repository/archive.zip?ref=master)
| `OTA`           | *固件升级和远程配置*                        | [OTA组件下载链接](https://code.aliyun.com/linksdk/linksdk-ota/repository/archive.zip?ref=master)
| `Data-Model`    | *使用属性, 事件, 服务构成的物模型描述设备*  | [Data-Model组件下载链接](https://code.aliyun.com/linksdk/linksdk-data-model/repository/archive.zip?ref=master)
| `Dynreg`        | *在设备运行时分配`deviceSecret`以简化烧录*  | [Dynreg组件下载链接](https://code.aliyun.com/linksdk/linksdk-dynreg/repository/archive.zip?ref=master)
| `NTP`           | *基于MQTT协议从云平台获取标准时间*          | [NTP组件下载链接](https://code.aliyun.com/linksdk/linksdk-ntp/repository/archive.zip?ref=master)
| `Shadow`        | *基于MQTT协议获取或更新云端缓存模型*        | [Shadow组件下载链接](https://code.aliyun.com/linksdk/linksdk-shadow/repository/archive.zip?ref=master)
| `Logpost`       | *基于MQTT协议上报设备日志到云端控制台*      | [Logpost组件下载链接](https://code.aliyun.com/linksdk/linksdk-logpost/repository/archive.zip?ref=master)
| `Devinfo`       | *基于MQTT协议上报标签删除或标签更新请求*    | [Devinfo组件下载链接](https://code.aliyun.com/linksdk/linksdk-devinfo/repository/archive.zip?ref=master)

# SDK使用的最佳实践

为直观的了解SDK的移植和使用, 可点击链接访问以下的实际场景中开发文档记录, 参考官方给出的使用者角度最佳实践

## 移植实例

+ [乐鑫ESP8266移植](http://code.aliyun.com/linksdk/docs/wikis/best-practice/ESP8266_Porting)
+ [乐鑫ESP32移植](http://code.aliyun.com/linksdk/docs/wikis/best-practice/ESP32_Porting)
+ [MCU+TCP模组(SIM800C)移植](http://code.aliyun.com/linksdk/docs/wikis/best-practice/SIM800C_TCP_Porting)
+ [MCU+MQTT模组(N720V5)移植](http://code.aliyun.com/linksdk/docs/wikis/best-practice/N720V5_MQTT_Porting)
+ [Android源码树内移植](http://code.aliyun.com/linksdk/docs/wikis/best-practice/Android_Intree_Porting)
+ [Android源码树外NDK移植](http://code.aliyun.com/linksdk/docs/wikis/best-practice/Android_NDK_Porting)

## 特殊的TLS认证模式

+ [基于PSK的TLS连接](http://code.aliyun.com/linksdk/docs/wikis/best-practice/TLS_PSK_Auth)
+ [基于X509的TLS连接](http://code.aliyun.com/linksdk/docs/wikis/best-practice/TLS_X509_Auth)

# 编译方式

**`Link SDK`完全由高移植性的C语言源文件构成**, 用户应使用惯用的任意编译方式, 将这些C文件(`demos`目录除外)跟自己的其它源文件编译到一起即可使用它

---
*如果用户使用安装有`GNU Make`的`Linux`主机开发环境, 可在SDK源码根目录运行*

```
make
```

*编译SDK例程, 编好的例程在`output/xxxx_demo`, 运行这些例程可快速体验SDK和物联网平台的功能, 编程导引文档中也有例程的运行输出讲解*

# 设计原则

不论是MQTT连云这样放在`core`的SDK核心模块, 还是固件升级这样放在`components/xxx`的高阶组件, 一致使用以下的设计原则

+ 用户须知的API函数接口和数据结构, 在`xxx/aiot_xxx_api.h`头文件中列出, 以`aiot_xxx_yyy`风格命名
+ 这些API函数的实现源码, 在`xxx/aiot_xxx_api.c`中
+ 组件能力的使用范例, 在`xxx/demos/xxx_{basic,posix}_demo.c`中
+ 组件的API函数原型, 遵循统一的设计模式

    - `aiot_xxx_init()`: 初始化1个会话实例, 并设置默认参数
    - `aiot_xxx_deinit()`: 销毁1个会话实例, 回收其占用资源
    - `aiot_xxx_setopt()`: 配置1个会话实例的运行参数, 可用参数及用法在编程手册中有指出
    - `aiot_xxx_send_yyy()`: 向云平台发起某种会话请求
    - `aiot_xxx_recv()`: 从云平台接收请求的应答

+ 组件能力运行时, 对外表达信息的方式, 遵循统一的设计模式

    - **API的返回值**: 是1个`16 bits`的非正数整型, 也叫**状态码**, `0`表成功, 其它值表达运行状态
        * `retval = aiot_xxx_yyy()`方式获取返回值
        * 所有返回值唯一对应内部运行分支, 含义详见`core/aiot_state_api.h`或`components/xxx/aiot_xxx_api.h`
        * 所有组件的返回值的值域互不重叠, 共同分别分布在`0x0000 - 0xFFFF`
    - **数据回调函数**: 是1个用户实现并传入SDK的回调函数, SDK从外界读取到值得关注的数据报文时, SDK会调用它, 用户可在此处理数据流
        * `aiot_xxx_setopt(handle, AIOT_XXXOPT_RECV_HANDLER, user_recv_cb)`设置数据回调
    - **事件回调函数**: 是1个用户实现并传入SDK的回调函数, SDK内部运行状态发生值得关注的变化时, SDK会调用它, 用户可在此处理控制流
        * `aiot_xxx_setopt(handle, AIOT_XXXOPT_EVENT_HANDLER, user_event_cb)`设置事件回调
    - **运行日志回调**: 是1个用户实现并传入SDK的回调函数, SDK运行时, 详细的运行日志字符串会实时输入到这个回调
        * `aiot_state_set_logcb(user_log_cb)`设置日志回调
        * 若不想看到SDK运行日志, 回调为空即可
        * 日志格式统一为: `[timestamp][LK-XXXX] message`
            + `XXXX`以数字形式标识了日志字符串, 它和返回值共享一个**状态码**分布空间, 都在`-0xFFFF ~ 0x0000`
            + 利用SDK的高阶组件之一, 时间同步(`ntp`), 可进行网络对时, 此后日志中的`timestamp`会自动变成"年月日 时分秒"的易读模式

> [**点此查看详细状态码清单**](http://code.aliyun.com/linksdk/docs/wikis/prog-guide/StateCode_List), 比如`-0x0305`代表MQTT连云时设备鉴权失败

