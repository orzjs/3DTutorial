# 一些属性的解释

**声明: 因为3D属性浏览器的兼容性不好，所以在写3D变换的属性时记得加浏览器前缀-webkit-，-moz-等等。**

## transform-origin

**transform-origin: x-axis y-axis z-axis;**    

**x-axis**  定义视图被置于 X 轴的何处(left, center, right, length, %)     

**y-axis**  定义视图被置于 Y 轴的何处(left, center, right, length, %)    

**z-axis**  定义视图被置于 Y 轴的何处(length)    

**通俗来讲，就是做2D/3D变换所绕的轴的位置。**    

[查看演示](http://www.w3school.com.cn/example/css3/demo_css3_transform-origin.html)    

## Perspective

**要显示3D效果必须要有这个属性！**    

Perspective, 即透视，咳。。    
用于定义 3D 元素距视图的距离，以像素计。    
当为元素定义 perspective 属性时，其子元素会获得透视效果，而不是元素本身。所以我们可以定义一个container，作为父元素，定义perspective属性即可。    

为了更通俗的理解，看一张图(转自张鑫旭)：

![perspective](img/3d-distance.jpg)    

**两种定义方式，transform: perspective( 600px )或perspective: 600px**

[查看演示](http://www.zhangxinxu.com/study/201209/transform-perspective-translateZ.html)    

## perspective-origin

perspective-origin 属性定义 3D 元素所基于的 X 轴和 Y 轴。该属性允许您改变 3D 元素的底部位置。该属性必须与 perspective 属性一同使用。    

**通俗来讲，就是我们视角所在的位置。**    

[查看演示](http://www.runoob.com/try/try.php?filename=trycss3_perspective-origin_inuse)    


