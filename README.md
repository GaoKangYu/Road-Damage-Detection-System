# Road-Damage-Detection-System
“道路损伤检测”项目
## 背景/需求
-   路面病害对道路和行车安全构成潜在威胁，而至今没有具有高度适用性的自动化测量仪器可以使用。传统方法为人工目测排查，费时费力，数据的可比性和重复性都较差。
-   项目选取车载相机或手机拍摄的路面图像为研究对象，基于[RDDC2020](https://github.com/sekilab/RoadDamageDetector)数据集，使用三种卷积神经网络（Fcos、FasterRcnn、YOLO v3）实现了道路损伤检测系统。
-   本项目包含可执行演示系统和模型训练部分配置文件
![demo_ui](https://github.com/GaoKangYu/Road-Damage-Detection-System/blob/main/demo_ui_img/ui.png)
![dataset_composition](https://github.com/GaoKangYu/Road-Damage-Detection-System/blob/main/demo_ui_img/dataset_composition.png)
## 环境需求
-   Windows(demo) and Linux(model training)
-   Python 3.5+
-   CMake >= 3.12
-   CUDA >= 8.0
-   OpenCV >= 2.4
-   cuDNN >= 7.0
-   on Linux  **GCC or Clang**, on Windows  **MSVC 2017/2019**  
## 文件结构

文件结构及其作用如下：

```
Road-Damage-Detection-System
├── Demo(基于QT C++开发的客户端演示系统，部分DLL库和权重文件由于体积过大存于网盘)
├── Demo_ui_img(系统演示截图)
├── experiment(包含训练三个模型的配置文件、mAP图表、权重等)
├── test_data(测试数据，包含视频、图片)
├── demo screen record(系统演示录屏)
```
- 部分缺失权重和DLL配置文件下载地址
链接：https://pan.baidu.com/s/1M2n56VVLIbiGppXL4dDwzw 
提取码：LZNT
## 功能示意
- 选取并导入图片
![load_img](https://github.com/GaoKangYu/Road-Damage-Detection-System/blob/main/demo_ui_img/load_img.png)
- 选取并导入视频
![load_video](https://github.com/GaoKangYu/Road-Damage-Detection-System/blob/main/demo_ui_img/load_video.png)
- 检测图片
![img_detect_result](https://github.com/GaoKangYu/Road-Damage-Detection-System/blob/main/demo_ui_img/img_detect_result.png)
- 检测视频
![video_detect_result](https://github.com/GaoKangYu/Road-Damage-Detection-System/blob/main/demo_ui_img/video_detect_result.png)
## 性能指标
-  模型表现(基于linux，GTX 1080ti)
![model_performance](https://github.com/GaoKangYu/Road-Damage-Detection-System/blob/main/demo_ui_img/model_performance.png)
-  模型表现(基于windows下demo，GTX 1660ti)
![model_performance_based_on_demo](https://github.com/GaoKangYu/Road-Damage-Detection-System/blob/main/demo_ui_img/model_performance_based_on_demo.png)
