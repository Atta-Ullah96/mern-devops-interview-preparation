# CSS Inheritance

## What is inheritance?

Inheritance means some CSS properties automatically pass from a parent element to child elements.

Example:

```html
<div class="parent">
  <p>This is a paragraph</p>
  <span>This is a span</span>
</div>
```

```css
.parent {
  color: blue;
  font-family: Arial, sans-serif;
}
```

Both `p` and `span` will inherit:

```txt
color: blue
font-family: Arial
```

## Why inheritance exists

Inheritance helps avoid repeating the same styles again and again.

Example:

```css
body {
  font-family: Arial, sans-serif;
  color: #333;
}
```

Now most text inside the page can inherit the same font and color.

## Common inherited properties

Text-related properties are usually inherited:

```txt
color
font-family
font-size
font-weight
line-height
text-align
visibility
```

Example:

```css
body {
  font-family: Arial, sans-serif;
  color: #222;
}
```

All normal text inside the body can inherit these values.

## Common non-inherited properties

Box model and layout-related properties are usually not inherited:

```txt
margin
padding
border
width
height
background
display
position
```

Example:

```css
.parent {
  padding: 20px;
  border: 1px solid black;
}
```

Child elements will not automatically inherit the same padding and border.

Why?

Because if every child inherited padding, margin, border, width, and height, layouts would break easily.

## Force inheritance

You can force an element to inherit a property using `inherit`.

Example:

```css
button {
  font-family: inherit;
}
```

This is common because buttons often have browser default fonts.

Example:

```css
body {
  font-family: Arial, sans-serif;
}

button {
  font-family: inherit;
}
```

Now the button uses the same font as the body.

## Initial value

You can reset a property to its default value using `initial`.

```css
p {
  color: initial;
}
```

## Unset value

`unset` behaves like:

```txt
inherit if the property is naturally inherited
initial if the property is not naturally inherited
```

Example:

```css
.box {
  color: unset;
  padding: unset;
}
```

## Interview answer

> Inheritance means some CSS properties automatically pass from parent elements to child elements. Text-related properties like `color`, `font-family`, `font-size`, and `text-align` are usually inherited. Box model properties like `margin`, `padding`, `border`, `width`, and `height` are usually not inherited. We can force inheritance using the `inherit` value.

## What I learned

- Inheritance passes some styles from parent to child.
- Text-related properties are usually inherited.
- Box model properties are usually not inherited.
- `inherit` can force a child to use the parent value.
- Inheritance helps reduce repeated CSS.
