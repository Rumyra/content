---
title: offset
slug: Web/CSS/offset
page-type: css-shorthand-property
browser-compat: css.properties.offset
---

{{CSSRef}}

The **`offset`** CSS [shorthand property](/en-US/docs/Web/CSS/CSS_cascade/Shorthand_properties) sets all the properties required for animating an element along a defined path. The offset properties together help to define an _offset transform_, a [transform](/en-US/docs/Web/CSS/CSS_transforms/Using_CSS_transforms) that aligns a point in an element ([offset-anchor](/en-US/docs/Web/CSS/offset-anchor)) to an _offset position_ ([offset-position](/en-US/docs/Web/CSS/offset-position)) on a path ([offset-path](/en-US/docs/Web/CSS/offset-path)) at various points along the path ([offset-distance](/en-US/docs/Web/CSS/offset-distance)) and optionally rotates the element ([offset-rotate](/en-US/docs/Web/CSS/offset-rotate)) to follow the direction of the path.

> [!NOTE]
> Early versions of the spec called this property `motion`.

{{EmbedInteractiveExample("pages/css/offset.html")}}

## Constituent properties

This property is a shorthand for the following CSS properties:

- {{cssxref("offset-anchor")}}
- {{cssxref("offset-distance")}}
- {{cssxref("offset-path")}}
- {{cssxref("offset-position")}}
- {{cssxref("offset-rotate")}}

## Syntax

```css
/* Offset position */
offset: auto;
offset: 10px 30px;
offset: none;

/* Offset path */
offset: ray(45deg closest-side);
offset: path("M 100 100 L 300 100 L 200 300 z");
offset: url(arc.svg);

/* Offset path with distance and/or rotation */
offset: url(circle.svg) 100px;
offset: url(circle.svg) 40%;
offset: url(circle.svg) 30deg;
offset: url(circle.svg) 50px 20deg;

/* Including offset anchor */
offset: ray(45deg closest-side) / 40px 20px;
offset: url(arc.svg) 2cm / 0.5cm 3cm;
offset: url(arc.svg) 30deg / 50px 100px;

/* Global values */
offset: inherit;
offset: initial;
offset: revert;
offset: revert-layer;
offset: unset;
```

## Formal definition

{{cssinfo}}

## Formal syntax

{{csssyntax}}

## Examples

### Animating an element along a path

#### HTML

```html
<div id="offsetElement"></div>
```

#### CSS

```css
@keyframes move {
  from {
    offset-distance: 0%;
  }

  to {
    offset-distance: 100%;
  }
}

#offsetElement {
  width: 50px;
  height: 50px;
  background-color: blue;
  offset: path("M 100 100 L 300 100 L 200 300 z") auto;
  animation: move 3s linear infinite;
}
```

#### Result

{{EmbedLiveSample("Animating_an_element_along_a_path", 350, 350)}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{cssxref("offset-anchor")}}
- {{cssxref("offset-distance")}}
- {{cssxref("offset-path")}}
- {{cssxref("offset-position")}}
- {{cssxref("offset-rotate")}}
