TOPICS: <ruby>
        <rp>
        <rt>
        <rb>
        <rtc>
AUTHORS: Wizard; wizardforcel@mozilla.net; mdn:wizardforcel
         Yuyang ZHOU; Martin.Chow@mozilla.net; mdn:Martin.Chow
         Yujiyang; Yujiyang@github.com; github:Yujiyang
         yumin; richardminyu@foxmail.com; github:richardmyu
         Hodor Jorn; zhaohaodang@mozilla.net; mdn:zhaohaodang

# `<ruby>`

**HTML `<ruby>` 元素** 被用来展示东亚文字注音或字符注释。

|  |  |
| :-- | :-- |
| **内容范畴** | 流式内容, 短语内容, 明显的内容. |
| **允许内容** | 短语内容 |
| **标签省略** | 不允许，开始标签和结束标签都不能省略。|
| **允许的父级元素** | 见散文 |
| **DOM 接口** | `HTMLElement` |

## 属性

本元素支持 全局属性。

## `<rp>`

**HTML `<rp>` 元素**用于为那些不能使用 `<ruby>` 元素展示 ruby 注解的浏览器，提供随后的圆括号。

|  |  |
| :-- | :-- |
| **内容分类** | 无 |
| **允许的内容** | 文本 |
| **标签省略** | 不允许，开始标签和结束标签都不能省略。|
| **允许的父元素** | `<ruby>` 元素。 `<rp>` 必须位于 `<rt>` 的前面和后面。 |
| **允许的 ARIA 角色** | 任意 |
| **DOM 接口** | `HTMLElement` |

用法注解

- Ruby 注解用于展示东亚文字的发音，例如使用日语罗马音和汉语拼音的文字。 `<rp>` 元素用于不支持 `<ruby>` 元素的情况。 `<rp>` 的内容提供了应该展示的东西，通常是圆括号，
以便表示 ruby 注解的存在。

## `<rt>`

**HTML Ruby 文本 (`<rt>`) 元素**包含字符的发音，字符在 ruby 注解中出现，它用于描述东亚字符的发音。这个元素始终在 `<ruby>` 元素中使用。

|  |  |
| :-- | :-- |
| **内容分类** | 无 |  
| **允许的内容** | 短语内容 |
| **标签省略** | 如果 `<rt>` 元素紧紧跟随  `<rt>` 或者 `<rp>` 元素，或者父元素中没有更多内容了，结束标签可以省略。|
| **允许的父元素** | `<ruby>` 元素 |
| **允许的 ARIA 角色** | 任意 |  
| **DOM 接口** | `HTMLElement` |

## `<rb>`

HTML Ruby 基础（`<rb>`）元素用于分隔`<ruby>`注释的基本文本组件（即正在注释的文本）。一个`<rb>`元素应该包装基本文本的每个单独的原子段。

|  |  |
| :-- | :-- |
| **内容分类** | 无 |  
| **允许的内容** | 作为 `<ruby>` 元素的子元素。 |
| **标签省略** | 如果元素紧跟`<rt>`、`<rtc>`或`<rp>`元素或其他元素，则可省略结束标记 `<rb>`元素，或者如果父元素中没有其他内容。 |
| **允许的父元素** | `<ruby>` 元素 |
| **允许的 ARIA 角色** | 任意 |  
| **DOM 接口** | `HTMLElement` |

用法注解

- Ruby 注解用于展示东亚文字的发音，例如使用日语罗马音和汉语拼音的文字。 `<rb>` 元素用于分隔出ruby基本文本的每个片段。
- 虽然 `<rb>` 不是一个空元素，但是在源码中通常只包括每个元素的开始标签。 因此ruby标记就不那么复杂，也更容易阅读。在渲染版本中，浏览器也可以填充完整的元素。
- 你需要为要注释的每个基本段（`<rb>`元素）包含一个`<rt>`元素。

## `<rtc>`

**HTML `<rtc>` 元素**包含文字的语义注解，它们在 `<rb>` 元素中展示。`<rb>` 元素可以拥有发音 (`<rt>`) 和语义(`<rtc>`) 注解。

## 示例

### 示例1: 字节

```html
<ruby>
  漢 <rp>(</rp><rt>Kan</rt><rp>)</rp>
  字 <rp>(</rp><rt>ji</rt><rp>)</rp>
</ruby>
```

### 示例2: 词节

```html
<ruby>
  明日 <rp>(</rp><rt>Ashita</rt><rp>)</rp>
</ruby>
```

### 示例3

```html
<ruby>
  <rb>漢</rb>字
  <rp>(</rp><rt>kan</rt>ji<rp>)</rp>
</ruby>
```

### 示例4

```html
<ruby>
   <rb>旧</rb>
   <rb>金</rb>
   <rb>山</rb>
   <rt>jiù</rt>
   <rt>jīn</rt>
   <rt>shān</rt>
   <rtc>San Francisco</rtc>
</ruby>
```
