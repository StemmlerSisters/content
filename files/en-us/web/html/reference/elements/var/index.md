---
title: "<var>: The Variable element"
slug: Web/HTML/Reference/Elements/var
page-type: html-element
browser-compat: html.elements.var
sidebar: htmlsidebar
---

The **`<var>`** [HTML](/en-US/docs/Web/HTML) element represents the name of a variable in a mathematical expression or a programming context. It's typically presented using an italicized version of the current typeface, although that behavior is browser-dependent.

{{InteractiveExample("HTML Demo: &lt;var&gt;", "tabbed-shorter")}}

```html interactive-example
<p>
  The volume of a box is <var>l</var> × <var>w</var> × <var>h</var>, where
  <var>l</var> represents the length, <var>w</var> the width and
  <var>h</var> the height of the box.
</p>
```

```css interactive-example
var {
  font-weight: bold;
}
```

## Attributes

This element only includes the [global attributes](/en-US/docs/Web/HTML/Reference/Global_attributes).

## Usage notes

### Related elements

Other elements that are used in contexts in which `<var>` is commonly used include:

- {{HTMLElement("code")}}: The HTML Code element
- {{HTMLElement("kbd")}}: The HTML Keyboard input element
- {{HTMLElement("samp")}}: The HTML Sample Output element

If you encounter code that is mistakenly using `<var>` for style purposes rather than semantic purposes, you should either use a {{HTMLElement("span")}} with appropriate CSS or, an appropriate semantic element among the following:

- {{HTMLElement("em")}}
- {{HTMLElement("i")}}
- {{HTMLElement("q")}}

### Default style

Most browsers apply {{cssxref("font-style")}} to `"italic"` when rendering `<var>`. This can be overridden in CSS, like this:

```css
var {
  font-style: normal;
}
```

## Examples

### Basic example

Here's a basic example, using `<var>` to denote variable names in a mathematical equation.

```html
<p>An algebraic equation: <var>x</var> = <var>y</var> + 2</p>
```

#### Result

{{EmbedLiveSample("Basic_example", 650,80)}}

### Overriding the default style

Using CSS, you can override the default style for the `<var>` element. In this example, variable names are rendered in bold, using Courier if it's available, otherwise it falls back to the default monospace font.

#### CSS

```css
var {
  font:
    bold 15px "Courier",
    "Courier New",
    monospace;
}
```

#### HTML

```html
<p>
  The variables <var>minSpeed</var> and <var>maxSpeed</var> control the minimum
  and maximum speed of the apparatus in revolutions per minute (RPM).
</p>
```

This HTML uses `<var>` to enclose the names of two variables.

#### Result

{{EmbedLiveSample("Overriding_the_default_style", 650, 140)}}

## Technical summary

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">
        <a href="/en-US/docs/Web/HTML/Guides/Content_categories"
          >Content categories</a
        >
      </th>
      <td>
        <a href="/en-US/docs/Web/HTML/Guides/Content_categories#flow_content"
          >Flow content</a
        >,
        <a href="/en-US/docs/Web/HTML/Guides/Content_categories#phrasing_content"
          >phrasing content</a
        >, palpable content.
      </td>
    </tr>
    <tr>
      <th scope="row">Permitted content</th>
      <td>
        <a href="/en-US/docs/Web/HTML/Guides/Content_categories#phrasing_content"
          >Phrasing content</a
        >.
      </td>
    </tr>
    <tr>
      <th scope="row">Tag omission</th>
      <td>None, both the starting and ending tag are mandatory.</td>
    </tr>
    <tr>
      <th scope="row">Permitted parents</th>
      <td>
        Any element that accepts
        <a href="/en-US/docs/Web/HTML/Guides/Content_categories#phrasing_content"
          >phrasing content</a
        >.
      </td>
    </tr>
    <tr>
      <th scope="row">Implicit ARIA role</th>
      <td>
        <a href="https://w3c.github.io/html-aria/#dfn-no-corresponding-role"
          >No corresponding role</a
        >
      </td>
    </tr>
    <tr>
      <th scope="row">Permitted ARIA roles</th>
      <td>Any</td>
    </tr>
    <tr>
      <th scope="row">DOM interface</th>
      <td>{{domxref("HTMLElement")}}</td>
    </tr>
  </tbody>
</table>

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
