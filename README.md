桥梁病害检测数据集，6700张，支持YOLO格式
适合做桥梁病害检测、结构健康监测、图像分析相关研究用，数据很全，直接可用

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7b67b7b5170e417297cede6155de5097.png)

标签：
生物降解
混凝土浸出
裂缝
泛碱
钢筋外露
模板凹槽
污渍或渗透![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7d31512bb4c44e2a9f0245ccfcb8d885.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b037b59578e34cdf88fc8259482a96a0.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/8ce9bbef4649496087a932ec753db1fa.png)
# 桥梁病害检测数据集
|项目|详情|
| ---- | ---- |
|数据集名称|桥梁病害检测数据集|
|标注格式|YOLO TXT标注|
|样本总量|6700张|
|适用场景|桥梁病害自动识别、桥梁结构健康监测、基础设施巡检、视觉检测算法研发|

### 类别明细
|类别ID|类别名称|
| ---- | ---- |
|0|生物降解|
|1|混凝土浸出|
|2|裂缝|
|3|泛碱|
|4|钢筋外露|
|5|模板凹槽|
|6|污渍或渗透|

### 应用价值
无人机/摄像头桥梁巡检场景，自动识别各类混凝土表观病害，替代人工目视排查，适合路政、交通工程、智慧基建方向YOLO检测模型训练。
```python
# YOLOv11n训练脚本
from ultralytics import YOLO

if __name__ == '__main__':
    model = YOLO("yolov11n.pt")
    model.train(
        data="bridge_defect.yaml",
        epochs=80,
        imgsz=640,
        batch=8,
        device=0
    )
```

