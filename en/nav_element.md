TOPICS: <nav>
AUTHORS: Eric Bailey; ericwbailey@github.com; github:ericwbailey
         Tang Yun; ntutangyun@gmail.com; github:ntutangyun
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Sphinx; SphinxKnight@github.com; github:SphinxKnight
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Teoli; teoli@mozilla.net; mdn:teoli
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Sebastian Zartner; SebastianZ@github.com; github:SebastianZ
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Peter; pwdst@mozilla.net; mdn:pwdst
         Keiichi; ethertank@mozilla.net; mdn:ethertank
         Christian Sonne; cers@mozilla.net; mdn:cers
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Jonathan Wilsson; jwilsson@github.com; github:jwilsson
         Trevor Hobson; trevorhobson@github.com; github:trevorhobson
         Janet Swisher; jmswisher@github.com; github:jmswisher

# `<nav>`

The **HTML `<nav>` element** represents a section of a page whose purpose is to provide navigation
links, either within the current document or to other documents. Common examples of navigation
sections are menus, tables of contents, and indexes.

|  |  |
| :-- | :-- |
| **Content categories** | Flow content, sectioning content, palpable content. |
| **Permitted content** | Flow content. |
| **Tag omission** | None, both the starting and ending tag are mandatory.|
| **Permitted parents** | Any element that accepts flow content.
| **Permitted ARIA roles** | None |
| **DOM interface** | `HTMLElement` |

## Attributes

This element only includes the [global attributes](https://wiki.developer.mozilla.org/en-US/docs/HTML/Global_attributes).

## Usage Notes

- It's not necessary for all links to be contained in a `<nav>` element. `<nav>` is intended only
for major block of navigation links; typically the [`<footer>`](/en/webfrontend/<footer>) element
often has a list of links that don't need to be in a `<nav>` element.
- A document may have several `<nav>` elements, for example, one for site navigation and one for
intra-page navigation. aria-labelledby can be used in such case to promote accessibility, see example.
- User agents, such as screen readers targeting disabled users, can use this element to determine
whether to omit the initial rendering of navigation-only content.

## Examples

In this example, a `<nav>` block is used to contain an unordered list
([`<ul>`](/en/webfrontend/<ul>)) of links.
With appropriate CSS, this can be presented as a sidebar, navigation bar, or drop-down menu.

```html
<nav class="menu">
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">About</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>
```
