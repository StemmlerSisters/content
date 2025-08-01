---
title: matrix()
slug: Web/CSS/transform-function/matrix
page-type: css-function
browser-compat: css.types.transform-function.matrix
sidebar: cssref
---

The **`matrix()`** [CSS](/en-US/docs/Web/CSS) [function](/en-US/docs/Web/CSS/CSS_Values_and_Units/CSS_Value_Functions) defines a homogeneous 2D transformation matrix. Its result is
a {{cssxref("&lt;transform-function&gt;")}} data type.

> [!NOTE]
> The `matrix(a, b, c, d, tx, ty)` function is a shorthand for `matrix3d(a, b, 0, 0, c, d, 0, 0, 0, 0, 1, 0, tx, ty, 0, 1)`.

{{InteractiveExample("CSS Demo: matrix()")}}

```css interactive-example-choice
transform: matrix(1.2, 0.2, -1, 0.9, 0, 20);
```

```css interactive-example-choice
transform: matrix(0.4, 0, 0.5, 1.2, 60, 10);
```

```css interactive-example-choice
transform: matrix(0, 1, 1, 0, 0, 0);
```

```css interactive-example-choice
transform: matrix(0.1, 1, -0.3, 1, 0, 0);
```

```html interactive-example
<section id="default-example">
  <img
    class="transition-all"
    id="example-element"
    src="/shared-assets/images/examples/firefox-logo.svg"
    width="200" />
</section>
```

## Syntax

```css
matrix(a, b, c, d, tx, ty)
```

### Values

The `matrix()` function is specified with six values. The constant values are implied and not passed as
parameters; the other parameters are described in the column-major order.

- _a_ _b_ _c_ _d_
  - : Are {{cssxref("&lt;number&gt;")}}s describing the linear transformation.
- _tx_ _ty_
  - : Are {{cssxref("&lt;number&gt;")}}s describing the translation to apply.

<table class="standard-table">
  <thead>
    <tr>
      <th scope="col"><a href="/en-US/docs/Web/CSS/transform-function#cartesian_coordinates">Cartesian coordinates</a> on <a href="https://en.wikipedia.org/wiki/Real_coordinate_space">ℝ^2</a></th>
      <th scope="col"><a href="https://en.wikipedia.org/wiki/Homogeneous_coordinates">Homogeneous coordinates</a> on <a href="https://en.wikipedia.org/wiki/Real_projective_plane">ℝℙ^2</a></th>
      <th scope="col">Cartesian coordinates on <a href="https://en.wikipedia.org/wiki/Real_coordinate_space">ℝ^3</a></th>
      <th scope="col">Homogeneous coordinates on <a href="https://en.wikipedia.org/wiki/Real_projective_space">ℝℙ^3</a></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">
        <math display="block">
          <semantics><mrow><mo>(</mo><mtable><mtr><mtd><mi>a</mi></mtd><mtd><mi>c</mi></mtd></mtr><mtr><mtd><mi>b</mi></mtd><mtd><mi>d</mi></mtd></mtr></mtable><mo>)</mo></mrow><annotation encoding="TeX">\begin{pmatrix} a & c \\ b & d \end{pmatrix}</annotation></semantics>
        </math>
      </td>
      <td>
        <math display="block">
          <semantics><mrow><mo>(</mo><mtable><mtr><mtd><mi>a</mi></mtd><mtd><mi>c</mi></mtd><mtd><mi>tx</mi></mtd></mtr><mtr><mtd><mi>b</mi></mtd><mtd><mi>d</mi></mtd><mtd><mi>ty</mi></mtd></mtr><mtr><mtd><mn>0</mn></mtd><mtd><mn>0</mn></mtd><mtd><mn>1</mn></mtd></mtr></mtable><mo>)</mo></mrow><annotation encoding="TeX">\left( \begin{array}{ccc} a & c & tx \\ b & d & ty \\ 0 & 0 & 1 \\ \end{array} \right)</annotation></semantics>
        </math>
      </td>
      <td rowspan="2">
        <math display="block">
          <semantics><mrow><mo>(</mo><mtable><mtr><mtd><mi>a</mi></mtd><mtd><mi>c</mi></mtd><mtd><mi>tx</mi></mtd></mtr><mtr><mtd><mi>b</mi></mtd><mtd><mi>d</mi></mtd><mtd><mi>ty</mi></mtd></mtr><mtr><mtd><mn>0</mn></mtd><mtd><mn>0</mn></mtd><mtd><mn>1</mn></mtd></mtr></mtable><mo>)</mo></mrow><annotation encoding="TeX">\left( \begin{array}{ccc} a & c & tx \\ b & d & ty \\ 0 & 0 & 1 \\ \end{array} \right)</annotation></semantics>
        </math>
      </td>
      <td rowspan="2">
        <math display="block">
          <semantics><mrow><mo>(</mo><mtable><mtr><mtd><mi>a</mi></mtd><mtd><mi>c</mi></mtd><mtd><mn>0</mn></mtd><mtd><mi>tx</mi></mtd></mtr><mtr><mtd><mi>b</mi></mtd><mtd><mi>d</mi></mtd><mtd><mn>0</mn></mtd><mtd><mi>ty</mi></mtd></mtr><mtr><mtd><mn>0</mn></mtd><mtd><mn>0</mn></mtd><mtd><mn>1</mn></mtd><mtd><mn>0</mn></mtd></mtr><mtr><mtd><mn>0</mn></mtd><mtd><mn>0</mn></mtd><mtd><mn>0</mn></mtd><mtd><mn>1</mn></mtd></mtr></mtable><mo>)</mo></mrow><annotation encoding="TeX">\left( \begin{array}{cccc} a & c & 0 & tx \\ b & d & 0 & ty \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1 \\ \end{array} \right)</annotation></semantics>
        </math>
      </td>
    </tr>
    <tr>
      <td><code>[a b c d tx ty]</code></td>
    </tr>
  </tbody>
</table>

The values represent the following functions:
`matrix(scaleX(), skewY(), skewX(), scaleY(), translateX(), translateY())`.

## Formal syntax

{{CSSSyntax}}

## Examples

### HTML

```html
<div>Normal</div>
<div class="changed">Changed</div>
```

### CSS

```css
div {
  width: 80px;
  height: 80px;
  background-color: skyblue;
}

.changed {
  transform: matrix(1, 2, -1, 1, 80, 80);
  background-color: pink;
}
```

### Result

{{EmbedLiveSample("Examples", 350, 350)}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{cssxref("transform")}}
- Individual transform properties:
  - {{cssxref("translate")}}
  - {{cssxref("scale")}}
  - {{cssxref("rotate")}}
- {{cssxref("&lt;transform-function&gt;")}}
- [`matrix3d()`](/en-US/docs/Web/CSS/transform-function/matrix3d)
