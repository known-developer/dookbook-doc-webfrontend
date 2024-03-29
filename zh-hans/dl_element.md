TOPICS: <dl>
        <dt>
        <dd>
AUTHORS: wenchuyang; wenchuyang@github.com; github:wenchuyang
         庄引; zhuangyin8@gmail.com; github:zhuangyin8
         Teoli; teoli@mozilla.net; mdn:teoli
         潘韬; pantao@mozilla.net; mdn:pantao
         Dong WEI; FredWe@mozilla.net; mdn:FredWe

# `<dl>`

**HTML `<dl>` 元素** （或 HTML 描述列表元素）是一个包含术语定义以及描述的列表，通常用于展示词汇表或者元数据 (键-值对列表)。

在 HTML5 之前， `<dl>` 被大家以定义列表所熟知。

|  |  |
| :-- | :-- |
| **内容分类** | 流内容，如果元素`<dl>`的子元素包括一对名称/值对，则可显示内容。|
| **允许的内容** | 零个或多个`<dt>`元素，每个元素后接一个或多个`<dd>`元素。|
| **标签省略** | 不允许，开始标签和结束标签都不能省略。|
| **允许的父元素** | 接受流内容的任何元素。 |
| **DOM 接口** | `HTMLDListElement` |

## 属性

该元素包含全局属性。

## `<dt>`

**HTML `<dt>` 元素** （或 HTML 术语定义元素）用于在一个定义列表中声明一个术语。该元素仅能作为 `<dl>` 的子元素出现。通常在该元素后面会跟着 `<dd>` 元素， 然而，
多个连续出现的 `<dt>` 元素都将由出现在它们后面的第一个 `<dd>` 元素定义。

|  |  |
| :-- | :-- |
| **内容分类** | 没有 |
| **允许的内容** | 流内容，但是不能包含 [`<header>`](/zh-hans/webfrontend/<header>) 元素、[`<footer>`](/zh-hans/webfrontend/<footer>) 元素或者其他章节、标题内容。|
| **标签省略** | 必须有开标签。如果该元素后面紧跟着另一个 `<dd>` 元素，或者父元素中没有更多内容，则可以省略闭标签。|
| **允许的父元素** | 该元素需要出现在 `<dt>` 元素或者 `<dd>` 元素之前，并且在 `<dl>` 元素中。|
| **DOM 接口** | `HTMLElement` 直到Gecko 1.9.2（Firefox 4）（包括该版本），Firefox均为此元素实现`HTMLSpanElement`接口。|

## `<dd>`

**HTML `<dd>` 元素**（HTML 描述元素）用来指明一个描述列表  (`<dl>`) 元素中一个术语的描述。这个元素只能作为描述列表元素的子元素出现，并且必须跟着一个 `<dt>` 元素。

|  |  |
| :-- | :-- |
| **内容分类** | 没有 |
| **允许的内容** | 流内容 |
| **标签省略** | 必须有开标签。如果该元素后面紧跟着另一个 `<dd>` 元素，或者父元素中没有更多内容，则可以省略闭标签。|
| **允许的父元素** | 该元素需要出现在 `<dt>` 元素和 `<dd>` 元素之后，并且在一个 `<dl>` 元素里。|
| **DOM 接口** | `HTMLElement` |

| 属性 | 描述 |
| :-- | :-- |
| `nowrap` | 如果这个属性的值为 yes，那么定义的描述文字将不会包裹。默认值为 no。 |

## 示例

```html
<dl>
  <dt>Firefox</dt>
  <dd>A free, open source, cross-platform, graphical web browser
      developed by the Mozilla Corporation and hundreds of volunteers.
  </dd>
  <!-- other terms and definitions -->
</dl>
```
