# 颜色识别传感器

## 简介
颜色识别传感器可返回当前物体颜色的HUE值。

![](./images/05006_01.png)

## 特性
---
- RJ11端口设计，防止误插，易于使用。
## 技术规格
---

项目 | 参数 
:-: | :-: 
SKU|EF05006
接口|RJ11
接口类型|IIC
工作电压|3.3V
产品尺寸|55.8 x 23.8 mm





## 外形与定位尺寸
---


![](./images/05006_02.png)


## 快速上手
---

### 所需器材及连接示意图
---

- 如下图所示，将颜色识别传感器连接到哪吒扩展板的IIC端口，并将OLED显示屏连接到哪吒扩展板的IIC端口。


![](./images/05006_03.png)

## makecode编程
---

### 步骤 1
在MakeCode的代码抽屉中点击“高级”，查看更多代码选项。

![](./images/05001_04.png)

为了给颜色识别传感器编程，我们需要添加一个扩展库。在代码抽屉底部找到“扩展”，并点击它。这时会弹出一个对话框，搜索”PlanetX“，然后点击下载这个代码库。

![](./images/05001_05.png)

*注意：*如果你得到一个提示说一些代码库因为不兼容的原因将被删除，你可以根据提示继续操作，或者在项目菜单栏里面新建一个项目。
### 步骤 2
### 如图所示编写程序

![](./images/05006_06.png)


### 参考程序
请参考程序连接：[https://makecode.microbit.org/_1p18D0hiT4Py](https://makecode.microbit.org/_1p18D0hiT4Py)

你也可以通过以下网页直接下载程序，下载完成后即可开始运行程序。

<div style="position:relative;height:0;padding-bottom:70%;overflow:hidden;"><iframe style="position:absolute;top:0;left:0;width:100%;height:100%;" src="https://makecode.microbit.org/#pub:_1p18D0hiT4Py" frameborder="0" sandbox="allow-popups allow-forms allow-scripts allow-same-origin"></iframe></div>  
---

### 结果
- 通过OLED显示屏可以看到颜色识别传感器识别到的颜色。

## python编程
---


### 步骤 1
为了方便的使用python对行星系列传感进行编程，我们可以使用已经编写好的库[PlanetX_MicroPython]，只需要调用函数并修改参数即可实现对应的功能。

下载压缩包并解压[PlanetX_MicroPython](https://github.com/lionyhw/PlanetX_MicroPython/archive/master.zip)

推荐使用官方平台：[Python editor](https://python.microbit.org/v/2.0)进行编程

![](./images/05001_07.png)

为了给颜色识别传感器编程，我们需要添加color.py文件。点击Load/Save，然后点击Show Files（1）下拉菜单，再点击Add file在本地找到下载并解压完成的PlanetX_MicroPython文件夹，从中选择color.py添加进来。

![](./images/05001_08.png)
![](./images/05001_09.png)
![](./images/05006_10.png)

### 步骤 2
### 参考程序
```
from microbit import *
from color import *
color = COLOR()
while True:
    display.scroll(color.get_hue())
```


### 结果
- 通过micro:bit上的LED矩阵可以看到当前颜色HUE值。
## 相关案例
---

## 技术文档
---
