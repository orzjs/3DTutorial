# CSS33D    

## 需要知道的属性:

|属性名称|作用|
|---|---|
|transform|向元素应用 2D 或 3D 转换|
|transform-origin|允许你改变被转换元素的位置|
|transform-style|规定被嵌套元素如何在 3D 空间中显示|
|perspective|规定 3D 元素的透视效果|
|perspective-origin|规定 3D 元素的底部位|
|backface-visibility|定义元素在不面对屏幕时是否可见|

__transform的属性：__    

|属性名称|作用|
|---|---|
|translate3d(x,y,z)|定义在x轴y轴z轴上的转换|
|scale3d(x,y,z)|定义在x轴y轴z轴上的 3D 缩放转换|
|rotate3d(x,y,z,angle)|定义在x轴y轴z轴上的 3D 旋转|
|skew(x-angle,y-angle)|定义沿着 X 和 Y 轴的 2D 倾斜转换|
|perspective(n)|为 3D 转换元素定义透视视图|

**tip: 操作多个属性的都可以分解成操作单一属性的。**     
**如：translate3d(x,y,z) ---- translateX(x)  translateY(y)  translateZ(z)**
