# 学习SVG

> - SVG （Scalable Vector Graphics） 可以缩放的矢量图形。
> - 矢量图形是相对于位图来说的，位图是由像素点组成，放大会失真，矢量图形，放大是不会失真的。
> - SVG 使用 XML 格式定义图像。

##### SVG的优势：
- SVG 与 JPGE、GIF 等图像比起来，尺寸更小，且可压缩性更强。
- SVG 可以在任何分辨率下被高清的打印。不失真。
- SVG 图像中的文本是可选的，同时也是可搜索的（很适合制作地图）。
- SVG 文件是纯粹的 XML。

---

**首先先来一个svg的例子进行代码分析：**

```xml
	<?xml version="1.0" standalone="no"?>
    <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
    "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">

    <svg width="100%" height="100%" version="1.1" xmlns="http://www.w3.org/2000/svg">
    	<circle cx="100" cy="50" r="40" stroke="black" stroke-width="2" fill="red"/>
	</svg>

```
`保存为.svg格式的文件。用浏览器打开，就会看到一个红色的圆圈，边框是黑色的。`

代码分析：

1、 第一行是XML的声明。standalone这个属性，是规定svg文件是否独立的。这里no说明不是独立的。引用了下面的dtd文件。
2、 第二三行，就是引用了dtd文件，这个文件内包含了所有允许的SVG元素。
3、 下面就是SVG代码，是一组闭合标签。width和height属性是设置此svg文档的宽度和高度。version属性是该SVG文件使用的版本。xmlns属性定义SVG的命名空间。
4、 cricle 单标签用来创建一个圆，cx cy属性定义圆的中心坐标。 r属性为半径。 stroke是描边也就是图形的轮廓，边框。 fill是填充，就是形状内的颜色。

---

#### HTML中嵌入SVG：

- 使用iframe标签：

```xml
    <html>
    <body>

   	 <iframe src="demo.svg"  width="300" height="100" frameborder="0"></iframe>

    </body>
    </html>
```
- 使用object标签：

```xml
    <html>
    <body>

   	 <object data="demo.svg"  width="300" height="100" type="image/svg+xml"></object>

    </body>
    </html>
```
---
#### 正式走进SVG...

> SVG 已经有许多预定义好的形状元素，例如 circle 圆 rect 矩形 等 ，我们开发人员可以直接可以拿来主义！

| 预定义好的形状元素 | 标签元素 |
|--------|--------|
|     圆形   |    circle    |
|     矩形   |    rect    |
|     椭圆   |    elipse    |
|     线   |    line    |
|     折线   |    polyline    |
|     多边形   |    polygon    |
|     路径   |    path    |

