# FACE-DETECTION 


## Sketch:

You can use your images to run your projects and here I have footage that you can change at will to provide real-time face recognition .
### 介绍 

实用的边缘设备无锚人脸检测与对齐算法Centerface, 模型大小7.3M。
**CenterFace-small** 性能达到centerface的同时模型大小仅为2.3M。

 ![image](results/bl4.jpg)   


### 更新

- 添加ncnn和opencv的工程

### 准确性

- WIDER FACE val集结果:

Model Version|Easy Set|Medium Set|Hard Set
------|--------|----------|--------
FaceBoxes|0.840 |0.766 |0.395
FaceBoxes3.2×|0.798|0.802|0.715
RetinaFace-mnet|0.887|0.870|0.792
LFFD-v1|0.910|0.881|0.780
LFFD-v2|0.837|0.835|0.729
CenterFace|0.935|0.924|0.875
CenterFace-small|0.931|0.924|0.870

- WIDER FACE test集结果:

Model Version|Easy Set|Medium Set|Hard Set
------|--------|----------|--------
FaceBoxes|0.839 |0.763 |0.396
FaceBoxes3.2×|0.791|0.794|0.715
LFFD-v1|0.910|0.881|0.780
LFFD-v2|0.837|0.835|0.729
CenterFace|0.932|0.921|0.873

> - 模型的训练数据仅包含：WIDER FACE train set
> - **RetinaFace-mnet** (RetinaFace-MobileNet-0.25)，来自于非常好的工作[insightface](https://github.com/deepinsight/insightface)。
> - **LFFD-v1** 也是很好的工作[LFFD](https://github.com/YonghaoHe/A-Light-and-Fast-Face-Detector-for-Edge-Devices)。
> - CenterFace/CenterFace-small的测试方法是MULTI-SCALE，因为训练图像和测试图像尺度的不一致性，多尺度测试才能反应centerface的真实性能。
   不过，对于SIO(原图单次推理)，CenterFace在val集上也可以达到：92.2% (Easy), 91.1% (Medium) and 78.2%，
   而RetinaFace-mnet在val集上是：89.6% (Easy), 87.1% (Medium) and 68.1% 
   
> - 关于Evaluation的一些思考:[人脸检测小江湖](evaluation.md)。

- FDDB的结果:

Model Version|Disc ROC curves score
------|--------
RetinaFace-mnet|96.0@1000
LFFD-v1|97.3@1000
LFFD-v2|97.2@1000
CenterFace|98.0@1000
CenterFace-small|98.1@1000

## WHERE RUN?

* 
  python >=3.6
  numpy 
  opencv-python
  torchvision
  torch
  pytorch






### 贡献者：
 - [ywlife](https://github.com/ywlife)
 - [SyGoing](https://github.com/SyGoing)
 - [MirrorYuChen](https://github.com/MirrorYuChen)
