TOPICS: <canvas>
AUTHORS: Yuyang ZHOU; Martin.Chow@mozilla.net; mdn:Martin.Chow
         潘韬; pantao@mozilla.net; mdn:pantao
         King; King.521@mozilla.net; mdn:King.521
         紫云飞; ziyunfei@mozilla.net; mdn:ziyunfei

# `<canvas>`

`<canvas>`元素可被用来通过脚本（通常是JavaScript）绘制图形。比如,它可以被用来绘制图形,制作图片集合,甚至用来实现动画效果。你可以(也应该)在元素标签内写入可提供替代的的代码内容，这些内容将会在在旧的、不支持`<canvas>`元素的浏览器或是禁用了JavaScript的浏览器内渲染并展现。

更多关于`<canvas>`元素内容，参见[canvas元素讨论页面](https://wiki.developer.mozilla.org/en-US/docs/Web/API/Canvas_API).

## 属性

本元素支持 全局属性.

| 属性 | 描述 |
| :-- | :-- |
| `height` | 该元素占用空间的高度，以 CSS 像素（px）表示，默认为 150。 |
| `moz-opaque` | 通过设置这个属性，来控制canvas元素是否半透明。如果你不想canvas元素被设置为半透明，使用这个元素将可以优化浏览器绘图性能。 |
| `width` | 该元素占用空间的宽度，以 CSS 像素（px）表示，默认为 300。 |

## 注意事项

需要`</canvas>`标签节

不同于 `<img>` 元素,  `<canvas>`元素需要有闭合标签 (`</canvas>`).

设置画布(canvas)的大小节

可以通过CSS来控制`<canvas>`的大小。在渲染的过程中`<canvas>`元素中的内容会根据情况缩放来适应需要的大小。如果您发现`<canvas>`元素中展示的内容变形，您可以通过`<canvas>`自带的height和width属性进行相关设置，而不要使用CSS。

## 示例

```html
<canvas id="canvas" width="300" height="300">
  Sorry, your browser doesn't support the &lt;canvas&gt;

element.
</canvas>
```

如果你没有设置`<canvas>`元素的透明度，可以考虑使用moz-opaque属性。下面给出的示例代码可用于页面渲染优化。但需要您注意的是，这个属性目前还没有被推广开来，只能在基于Mozilla内核的浏览器内生效。

```html
<canvas id="mycanvas" moz-opaque></canvas>
```
