# 1.简介

车牌检测采用了retinanet网络结构，车牌识别采用了以MobileNetV3为backbone的RLnet网络结构。使用该应用，可得到图像或视频中的每个车牌的检测框以及车牌信息。

# 2.应用使用说明

## 2.1 使用帮助

```
"Usage: " << licence_det_rec.elf << "<kmodel_det> <obj_thresh> <nms_thresh> <input_mode> <kmodel_reco> <debug_mode>"

各参数释义如下：
kmodel_det      车牌检测 kmodel路径
obj_thresh      车牌检测 分数阈值
nms_thresh      车牌检测 非极大值抑制阈值
input_mode      本地图片(图片路径)/ 摄像头(None) 
kmodel_reco     车牌识别kmodel路径 
debug_mode      是否需要调试，0、1、2分别表示不调试、简单调试、详细调试
 
 #单图推理示例：licence_rec_image.sh
./licence_det.elf LPD_640.kmodel 0.1 0.2 test.jpg licence_reco.kmodel 0

 #视频流推理：licence_rec_isp.sh
./licence_det.elf LPD_320.kmodel 0.1 0.2 None licence_reco.kmodel 0
```



