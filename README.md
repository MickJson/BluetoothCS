# BluetoothCS

经典蓝牙连接。

Android蓝牙API简介
经典蓝牙(Classic Bluetooth)
经典蓝牙适用于电池使用强度较大的操作，例如Android之间流式传输和通信等(音频/文件等大数据)。 从Android 4.3(API 18)才有API支持低功耗蓝牙(BLE)。

经典蓝牙API如下:

android.bluetooth

.BluetoothA2dp 音频分发配置文件,高质量音频通过蓝牙连接和流式传输

.BluetoothAdapter 本地蓝牙适配器,是所有蓝牙交互的入口,发现设备,查询配对设备,创建BluetoothServerSocket侦听其他设备

.BluetoothAssignedNumbers

.BluetoothClass 描述蓝牙设备的一般特征和功能,这是一组只读属性,设备类型提示

.BluetoothDevice 远程蓝牙设备,与某个远程设备建立连接,查询设备信息,名称,地址,类和配对状态

.BluetoothHeadset 提供蓝牙耳机支持,以便与手机配合使用,蓝牙耳机和免提配置文件

.BluetoothHealth 控制蓝牙服务的健康设备配置文件代理

.BluetoothHealthAppConfiguration 第三方蓝牙健康应用注册的应用配置，以便与远程蓝牙健康设备通信

.BluetoothHealthCallback 实现 BluetoothHealth 回调的抽象类

.BluetoothManager

.BluetoothProfile 蓝牙配置文件,蓝牙通信的无线接口规范

.BluetoothServerSocket 服务端监听,连接RFCOMM通道(类似TCP ServerSocket)

.BluetoothSocket 建立RFCOMM通道,蓝牙Socket接口(类似TCP Socket),通过InputStream和OutputStream与其他设备传输数据

Android经典蓝牙的开发步骤如下:

扫描其他蓝牙设备

查询本地蓝牙适配器的配对蓝牙设备

建立 RFCOMM 通道 (SPP协议)

通过服务发现连接到其他设备

与其他设备进行双向数据传输

管理多个连接

RFCOMM是蓝牙简单传输协议, 在两个蓝牙设备间的一条物理链上提供多个模拟串口进行传输数据, 可同时保持高达60路的通信连接。

SPP(Serial Port Profile)是通过蓝牙设备之间的串口进行数据传输协议，spp协议处于RFCOMM上层, 如果能使用RFCOMM传输数据,就不需要使用SPP(省去一些流程,速度更快),但还是推荐用SPP,兼容性有保证

博客地址：

[Android蓝牙开发（一）蓝牙模块及核心API](https://www.cnblogs.com/jqnl/p/13391663.html)

[Android蓝牙开发（二）经典蓝牙消息传输实现](https://www.jianshu.com/p/12395bfe4efb)
