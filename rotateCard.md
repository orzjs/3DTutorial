# 卡片翻转

相信大家都用过**网易云音乐**， 所以大家应该都对这个软件启动时候的翻转效果有印象。    

好多地方都会有类似的特效，如：http://unitedstack.github.io/    


今天这个demo也是如此，模拟**卡片的翻转**，先看demo:    

https://pengjiyuan.github.io/rotateCard/     

代码地址：https://github.com/PengJiyuan/rotateCard 

## 如何实现

### 1. 舞台

我们需要构建一个**舞台**，这个舞台是我们构建3D变换的一个容器。在这个场景下，我们可以想象成牌桌。    

```html
<div class="stage"></div>
```

这个容器我们需要设定一个**最重要**的属性--透视！    

`perspective: 800px;`    

加上这个属性，3D效果才起作用。    

### 2. 变换体

舞台构建完成之后，还需要一个做变换用的**载体**，在这个载体中，我们构建出需要的3D模型。在这个场景下，这个载体就是牌本身了。    

```html
<div class="container"></div>
```
在这个div中，我们需要设定同样重要的一个属性：

`transform-style: preserve-3d;`    

表示这个元素已3D的形式展示。

再加上过渡效果：    

`transition: all 1s;`    

### 3. 构建3D模型

在载体中，我们需要构建出来做变换用的**3D模型**。在这个场景中，也就是牌的正反面。    

```html
<div class="front"></div>    

<div class="back"></div>    
```

因为是正反面，所以是重叠在一起的，所以:    

`position: absolute;`    

为了更符合视觉效果，背面不可见。    

`backface-visibility: hidden;`     

背面是反向的，所以背面旋转180度。    

`transform: rotateY(180deg);`    

这样， 这张牌就构建好了。   

### 4. 卡片翻转

给翻转体添加点击事件，旋转180度，就可以完成点击翻转的效果。    
```css
.flip {
  transform: rotateY(-180deg);
}
```

```javascript
$('.stage').addEventListener('click', function() {
  this.classList.length === 1 ? this.classList.add('flip') : this.classList.remove('flip');
});
```    


**大功告成！**
