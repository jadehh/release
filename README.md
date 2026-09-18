#  Jade Tools C++ 工具合集 
## 更新时间 
2026-09-18 16:13:09 
# 更新日志

## v2.5.5

* 使用C++构建矩阵,支持行列的操作
* Json支持解析整数数组数组的参数
* 支持读取向量
* 新增SuperGlueOutput类, 用于存储SuperGlue的输出结果
* Docker环境统一加入opencv calib3d的功能,并升级CANN到6.0.1
* 删除opencv dnn的功能
* 修复Ascend上Crop图像的bug
* Ascend read Image 需要自动释放ImageProc和Context,也可以手动释放。
* 支持网络视频流,区分于相机的rtsp视频流,主要是Rtmp视频流,为了方便本地视频推流测试
* TODO 支持 JImage需要支持hconcat和vconcat操作，用于水平和垂直拼接图像
* JImage支持拼接操作
* 优化Ascend上图像拼接的性能,使用aclrtMemcpy2d函数操作,避免使用memcpy函数,提高拼接效率
* 新增Timer类, 用于测量代码执行时间
* 为了方便测试支持使用本地视频推流成rtsp视频流,模拟相机的rtsp视频流

---