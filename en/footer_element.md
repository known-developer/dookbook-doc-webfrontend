TOPICS: <footer>

# `<footer>`

The **HTML `<footer>` element** represents a footer for its nearest sectioning content or
sectioning root element. A footer typically contains information about the *author* of the
section, *copyright data* or *links to related documents*.

|  |  |
| :-- | :-- |
| **Content categories** | `Flow content`, `palpable content`.|
| **Permitted content** | `Flow content`, but with no `<footer>` or [`<header>`](/en/webfrontend/<header>) descendants.|
| **Tag omission** | None, both the starting and ending tag are mandatory.|
| **Permitted parents** | Any element that accepts `flow content`. Note that a `<footer>` element must not be a descendant of an [`<address>`](/en/webfrontend/<address>), [`<header>`](/en/webfrontend/<header>) or another `<footer>` element.|
| **Permitted ARIA roles** | `group`, `presentation` |
| **DOM interface** | `HTMLElement` |

## Attributes

This element only includes the [global attributes](https://wiki.developer.mozilla.org/en-US/docs/HTML/Global_attributes).

## Usage Notes

- Enclose information about the author in an [`<address>`](/en/webfrontend/<address>) element that
can be included into the `<footer>` element.
- The `<footer>` element is not sectioning content and therefore doesn't introduce a new section
in the outline.

## Examples

```html
<article>
  <!-- content here -->

  <footer>
    Some copyright info or perhaps some author info for an <code>&lt;article&gt;<code>?
    <address>Written by Li Yun.</address>
  </footer>
```
