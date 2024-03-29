TOPICS: <small>
AUTHORS: Taylor Hunt; tigt@github.com; github:tigt
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Sphinx; SphinxKnight@github.com; github:SphinxKnight
         Yuhei Yasuda; yuhei.yasuda1003@gmail.com; github:yuheiy
         Anton Ingfors; antoningfors@github.com; github:antoningfors
         Teoli; teoli@mozilla.net; mdn:teoli
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Thierry Régagnon; tregagnon@github.com; github:tregagnon
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Keiichi; ethertank@mozilla.net; mdn:ethertank
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Jonathan Wilsson; jwilsson@github.com; github:jwilsson

# `<small>`

The **HTML `<small>` element** makes the text font size one size smaller (for example, from large
to medium, or from small to x-small) down to the browser's minimum font size.  In HTML5, this
element is repurposed to represent side-comments and small print, including copyright and legal text,
independent of its styled presentation.

|  |  |
| :-- | :-- |
| **Content categories** | Flow content, phrasing content |
| **Permitted content** | Phrasing content |
| **Tag omission** | None, must have both a start tag and an end tag.|
| **Permitted parents** | Any element that accepts phrasing content, or any element that accepts flow content.|
| **Permitted ARIA roles** | Any |
| **DOM interface** | `HTMLElement` |

## Attributes

This element only includes the [global attributes](https://wiki.developer.mozilla.org/en-US/docs/HTML/Global_attributes).

!!! warn "Don't try this at home"
    **Implementation note:** up to Gecko 1.9.2 inclusive, Firefox implements the
    `HTMLSpanElement` interface for this element.

## Examples

### Example 1

```html
<p>This is the first sentence. <small>This whole sentence
  is in small letters.</small></p>
```

### Example 2 (CSS alternative)

```html
<p>This is the first sentence.
  <span style="font-size:0.8em;">This whole sentence is in small
  letters.</span></p>
```

## Notes

Although the `<small>` element, like the [`<b>`](/en/webfrontend/<b>) and
[`<i>`](/en/webfrontend/<i>) elements, may be perceived to violate the principle of separation
between structure and presentation, all three are valid in HTML5. Authors are encouraged to use
their best judgement when determining whether to use `<small>` or CSS.
