录制Intel RealSense D455彩色相机图、加速度计、陀螺仪数据。[参考代码自ORB_SLAM3](https://github.com/UZ-SLAMLab/ORB_SLAM3/tree/master/Examples/Monocular/recorder_realsense_D435i.cc)。

使用方法：

​	确保`path_to_saving_folder/IMU、path_to_saving_folder/cam0`目录存在

```shell
./recorder_realsense_D455 path_to_saving_folder
```



说明：

1. 各数据均带有单位为ns的时间戳
2. 本机实测彩色相机实拍图像和最终保存图像的时间戳大概相差150ms
3. 加速度计和陀螺仪的采样频率不一致，加速度计仅支持63/250HZ？陀螺仪支持200HZ？后续时间戳数据只要插值处理。