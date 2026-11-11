#  Jade Tools C++ 工具合集 
## 更新时间 
2026-11-11 16:51:07 
# 更新日志

## v2.5.7

* 加密狗登录支持docker -p 和 --net 启动, 分别对应本地登录和网络登录
* 监听加密狗的过程,使用加密狗的hasp_encrypt函数, 模拟加密操作,否则会话被自动释放
* 加密狗登录成功,监听加密狗的过程会提示已经拔掉加密狗,需要一并输出加密狗的ID,该bug在最早的系统中会出现
* 解决方式不使用--net启动Docker,加密狗开启网络功能
* 优化加密狗失败的提示信息
* 图片方式支持同步保存和异步保存,默认是同步保存
* 修复ModbusMonitorController::start()方法, 修复了在close()方法后, 再次调用start()方法, 会导致异常的问题
* 支持数据转换成base64编码的字符串, 用于保存json
* 支持Base64编码的字符串转换为数据, 用于从json中读取数据
* JImage支持设置GPU ID,并且通过getDeviceID方法获取当前使用的GPU ID
* JImage支持从GPU 0 拷贝到GPU 1, 用于图像的并行处理
* 图像裁剪操作也需要根据GPU ID进行裁剪, 用于在不同GPU上进行并行处理
* Matcher操作也支持使用GPU ID
* Device函数支持校验设置的设备 ID是否有效, 如果无效, 则默认使用第一个设备
* HaspAdapter支持网络功能,可以连接网络上的HaspAdapter设备
* 优化HaspAdapter的登录功能, 支持系统登录和网络登录
* linux上NVIDIAMonitor支持libnvidia-ml.so.1库, 用于获取GPU信息

---