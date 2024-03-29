TOPICS: <object>
AUTHORS: ExE Boss; ExE-Boss@github.com; github:ExE-Boss
         Masahiro Fujimoto; mfujimot@gmail.com; github:mfuji09
         Sphinx; SphinxKnight@github.com; github:SphinxKnight
         Teoli; teoli@mozilla.net; mdn:teoli
         Michael[tm] Smith; mike@w3.org; github:sideshowbarker
         Matijs Brinkhuis; matijs@mozilla.net; mdn:matijs
         Taylor Hunt; tigt@github.com; github:tigt
         Sebastian Zartner; SebastianZ@github.com; github:SebastianZ
         Maurizio; m32po@mozilla.net; mdn:m32po
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         J. McNair; J-Mackerel@mozilla.net; mdn:J-Mackerel
         Karen Scarfone; kscarfone@mozilla.net; mdn:kscarfone
         Thierry Régagnon; tregagnon@github.com; github:tregagnon
         Eric Shepherd; eshepherd@mozilla.com; github:a2sheppy
         Keiichi; ethertank@mozilla.net; mdn:ethertank
         Christian Sonne; cers@mozilla.net; mdn:cers
         Florian Scholz; fscholz@mozilla.net; mdn:fscholz
         Jonathan Wilsson; jwilsson@github.com; github:jwilsson
         Janet Swisher; jmswisher@github.com; github:jmswisher

# `<object>`

The **HTML `<object>` element** represents an external resource, which can be treated as an image,
a nested browsing context, or a resource to be handled by a plugin.

|  |  |
| :-- | :-- |
| **Content categories** | Flow content; phrasing content; embedded content, palpable content; if the element has a `usemap` attribute, interactive content; listed, submittable form-associated element.|
| **Permitted content** | zero or more [`<param>`](/en/webfrontend/<param>) elements, then transparent.|
| **Tag omission** | None, both the starting and ending tag are mandatory.|
| **Permitted parents** | Any element that accepts embedded content.|
| **Permitted ARIA roles** | `application`, `document`, `image` |
| **DOM interface** | `HTMLObjectElement` |

## Attributes

This element includes the [global attributes](https://wiki.developer.mozilla.org/en-US/docs/HTML/Global_attributes).

| Attribute | Description |
| :-- | :-- |
| `data` | The address of the resource as a valid URL. At least one of data and type must be defined.
| `form` | The form element, if any, that the object element is associated with (its form owner). The value of the attribute must be an ID of a `<form>` element in the same document.
| `height` | The height of the displayed resource, in CSS pixels. -- (Absolute values only. NO percentages)
| `name` | The name of valid browsing context (HTML5), or the name of the control (HTML 4).
| `type` | The content type of the resource specified by data. At least one of data and type must be defined.
| `typemustmatch` | This Boolean attribute indicates if the type attribute and the actual content type of the resource must match to be used.
| `usemap` | A hash-name reference to a [`<map>`](/en/webfrontend/<map>) element; that is a '#' followed by the value of a name of a map element.
| `width` | The width of the display resource, in CSS pixels. -- (Absolute values only. NO percentages)

## Examples

### Embed a flash movie

```html
<!-- Embed a flash movie -->
<object data="movie.swf"
  type="application/x-shockwave-flash"></object>

<!-- Embed a flash movie with parameters -->
<object data="movie.swf" type="application/x-shockwave-flash">
  <param name="foo" value="bar">
</object>
```
