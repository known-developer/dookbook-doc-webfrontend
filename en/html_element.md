TOPICS: <html>
        <html> lang attribute
        <html> Accessibility Concerns
        <head>
        HTML head element
        HTML head tag
        HTML5 Bone

# Root Element: `<html>`

The HTML `<html>` element represents the root (top-level element) of an [[HTML]] document, so it is also
referred to as the **root element**. All other elements must be descendants of this element.

## `<html>` Meta

|  |  |
| :-- | :-- |
| **Content categories** | None |
| **Permitted content** | One `<head>` element, followed by one [`<body>`](/en/webfrontend/<body>/) element.|
| **Tag omission** | The start tag may be omitted if the first thing inside the `<html>` element is not a comment. The end tag may be omitted if the `<html>` element is not immediately followed by a comment. |
| **Permitted parents** | None. This is the root element of a document. |
| **Permitted ARIA roles** | None |
| **DOM interface** | `HTMLHtmlElement` |

## HTML5 Bone

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Page Title</title>
</head>
<body>
  content
</body>
</html>
```

## `<html>` Attributes

This element includes the [global attributes](https://wiki.developer.mozilla.org/en-US/docs/HTML/Global_attributes).

| Attributes | Description |
| :--- | :--- |
| `xmlns` | Specifies the **XML Namespace** of the document. Default value is `"http://www.w3.org/1999/xhtml"`. This is required in documents parsed with XML parsers, and optional in `text/html` documents. |

## `<html>` Accessibility Concerns

Providing a `lang` attribute with a [valid IETF identifying language tag](https://www.ietf.org/rfc/bcp/bcp47.txt)
on the `<html>` element will help screen reading technology determine the proper language to
announce. The identifying language tag should describe the language used by the majority of the
content of the page. Without it, screen readers will typically default to the operating system's set
language, which may cause mispronunciations.

Including a valid `lang` declaration on the `<html>` element also ensures that important metadata
contained in the page's `<head>`, such as the page's [`<title>`](/en/webfrontend/<title>/), are also
announced properly.

- [MDN Understanding WCAG, Guideline 3.1 explanations](https://wiki.developer.mozilla.org/en-US/docs/Web/Accessibility/Understanding_WCAG/Understandable#Guideline_3.1_%E2%80%94_Readable_Make_text_content_readable_and_understandable)
- [Understanding Success Criterion 3.1.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/2016/NOTE-UNDERSTANDING-WCAG20-20161007/meaning-doc-lang-id.html)

## `<head>`

The HTML `<head>` element contains machine-readable information (**metadata**) about the document,
like its *title*, *author*, *description*, links to *scripts (JavaScript)*, and *style sheets (CSS)*
files that should be applied to the HTML.

!!! info
    **Note**: `<head>` primarily holds information for **machine processing**, not human-readability.
    For human-visible information, like top-level headings and listed authors, see the `<header>` element.

[[HTML5]]-compliant browsers automatically create a `<head>` element if its tags are omitted in the
markup. [This auto-creation is not guaranteed in ancient browsers](https://www.stevesouders.com/blog/2010/05/12/autohead-my-first-browserscope-user-test/).

### `<head>` Meta

|  |  |
| :-- | :-- |
| **Content categories** | None |
| **Permitted content** | If the document is an `<iframe>` `srcdoc` document, or if title information is available from a higher level protocol (like the subject line in HTML email), zero or more elements of metadata content.<br><br>Otherwise, one or more elements of metadata content where exactly one is a [`<title>`](/en/webfrontend/<title>/) element.|
| **Tag omission** | The start tag may be omitted if the first thing inside the `<head>` element is an element. The end tag may be omitted if the first thing following the `<head>` element is not a space character or a comment. |
| **Permitted parents** | An `<html>` element, as its first child.|
| **Permitted ARIA roles** | An `<html>` element, as its first child. |
| **DOM interface** | `HTMLHeadElement` |
