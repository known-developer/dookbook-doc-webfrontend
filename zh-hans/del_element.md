TOPICS: <del>

# `<del>`

HTML的`<del>`标签表示一些被从文档中删除的文字内容。比如可以在需要显示修改记录或者源代码差异的情况使用这个标签。[`<ins>`](/zh-hans/webfrontend/<ins>)标签的作用恰恰于此相反：表示文档中添加的内容。

这个标签通常（但不一定要）在文字上显示删除线。

|  |  |
| :-- | :-- |
| **内容分类** | 短语元素 或者 流式元素 。|
| **允许的内容** | 透明内容模型 |
| **标签省略** | 不允许，开始标签和结束标签都不能省略。|
| **允许的父元素** | 任意短语元素 |
| **允许的 ARIA 角色** | 任意 |
| **DOM 接口** | `HTMLModElement` |

## 属性

这个标签包含全局属性。

| 属性 | 描述 |
| :-- | :-- |
| `cite` | 提供一个URI，其中的资源解释作出修改的原因（比如：根据某次会议讨论）。 |
| `datetime` | 这个属性说明修改的时间和日期，这里的时间和日期格式要符合规范。如果设置的值不符合该规范，那么它将没有任何意义。 |

## 示例

```html
<p><del>This text has been deleted</del>, here is the rest of the paragraph.</p>
<del ><p >This paragraph has been deleted.</p ></del >
```
