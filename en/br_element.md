TOPICS: <br>
AUTHORS: Janet Swisher; jmswisher@github.com; github:jmswisher
         Christian Sonne; cers@mozilla.net; mdn:cers
         Keiichi; ethertank@mozilla.net; mdn:ethertank
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Sebastian Zartner; SebastianZ@github.com; github:SebastianZ
         Teoli; teoli@mozilla.net; mdn:teoli
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Yuhei Yasuda; yuhei.yasuda1003@gmail.com; github:yuheiy
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Chris Mills; chrisdavidmills@mozilla.net; mdn:chrisdavidmills
         Sphinx; SphinxKnight@github.com; github:SphinxKnight
         Eric Bailey; ericwbailey@github.com; github:ericwbailey
         Anton Ingfors; antoningfors@github.com; github:antoningfors
         Ward Muylaert; ward@mozilla.net; mdn:ward
         Nickolay Ponomarev; asqueella@gmail.com; github:nickolay

# `<br>`

The **HTML `<br>` element** produces a line break in text (carriage-return). It is useful for
writing a poem or an address, where the division of lines is significant.

As you can see from the above example, a `<br>` element is included at each point where we want the
text to break. The text after the `<br>` begins again at the start of the next line of the text block.

Note: Do not use `<br>` to create margins between paragraphs; wrap them in [`<p>`](/en/webfrontend/<p>)
elements and use the CSS] `margin` property to control their size.

## Attributes

This element's attributes include the [global attributes](https://wiki.developer.mozilla.org/en-US/docs/HTML/Global_attributes).

### Deprecated attributes

`clear`

Indicates where to begin the next line after the break.

## Styling with CSS

The `<br>` element has a single, well-defined purpose — to create a line break in a block of text.
As such, it has no dimensions or visual output of its own,
and there is very little you can do to style it.

You can set a `margin` on `<br>` elements themselves to increase the spacing between the
lines of text in the block, but this is a bad practice — you should use the
line-height property that was designed for that purpose.

## Examples

### Simple br

In the following example we use `<br>` elements to create
line breaks between the different lines of a postal address:

```html
Mozilla<br>
331 E. Evelyn Avenue<br>
Mountain View, CA<br>
94041<br>
USA<br>
```

## Accessibility Concerns

Creating separate paragraphs of text using `<br>` is not only bad practice, it is problematic for
people who navigate with the aid of screen reading technology. Screen readers may announce the
presence of the element, but not any content contained within `<br>`s. This can be a confusing and
frustrating experience for the person using the screen reader.

Use [`<p>`](/en/webfrontend/<p>) elements, and use CSS properties like `margin`
to control their spacing.

## Technical Summary

|  |  |
| :-- | :-- |
| **Content categories** | Flow content, phrasing content.|
| **Permitted content** | None, it is an empty element.|
| **Tag omission** | Must have a start tag, and must not have an end tag. In XHTML documents, write this element as `<br />`. |
| **Permitted parents** | Any element that accepts phrasing content.|
| **Permitted ARIA roles** | Any |
| **DOM interface** | `HTMLBRElement` |
