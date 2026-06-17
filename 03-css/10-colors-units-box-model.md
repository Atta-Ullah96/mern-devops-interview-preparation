# CSS Colors, Units and Box Model

## 1. What are CSS colors?

CSS colors are used to style text, backgrounds, borders, shadows, overlays, buttons, cards, and complete UI themes.

Example:

```css
h1 {
  color: #2563eb;
}

button {
  background-color: #2563eb;
  color: white;
}
```

## 2. Common CSS color formats

### Named colors

```css
.title {
  color: red;
}
```

Named colors are easy to remember, but they are not flexible enough for professional UI design.

### HEX colors

```css
.title {
  color: #2563eb;
}
```

HEX colors are very common in real projects.

### RGB colors

```css
.title {
  color: rgb(37, 99, 235);
}
```

RGB means red, green, and blue.

### RGBA colors

```css
.overlay {
  background-color: rgba(0, 0, 0, 0.5);
}
```

RGBA adds alpha/opacity. It is useful for overlays, modals, transparent backgrounds, and shadows.

### HSL colors

```css
.title {
  color: hsl(221, 83%, 53%);
}
```

HSL means hue, saturation, and lightness. It is useful when building design systems.

### CSS variables for colors

```css
:root {
  --primary-color: #2563eb;
  --text-color: #111827;
  --border-color: #e5e7eb;
}

button {
  background-color: var(--primary-color);
  color: white;
}
```

CSS variables help us keep colors consistent and easy to update.

## 3. What are CSS units?

CSS units define size. They are used for width, height, padding, margin, border, font-size, line-height, and spacing.

Example:

```css
.card {
  width: 320px;
  padding: 1.5rem;
  margin: 2rem auto;
}
```

## 4. Common CSS units

### px

`px` is a fixed/absolute unit.

```css
.card {
  border: 1px solid #e5e7eb;
}
```

Use `px` for borders, icons, shadows, and small fixed details.

### %

`%` is relative to the parent element.

```css
.child {
  width: 50%;
}
```

If the parent width is `1000px`, the child width becomes `500px`.

### rem

`rem` is relative to the root `html` font size.

Usually:

```txt
1rem = 16px
2rem = 32px
0.5rem = 8px
```

Example:

```css
h1 {
  font-size: 2rem;
}
```

### em

`em` is relative to the current element's font size. If the current element does not have a font size, it usually depends on the inherited parent font size.

```css
.parent {
  font-size: 20px;
}

.child {
  font-size: 2em; /* 40px */
}
```

### vh

`vh` is relative to viewport height.

```css
.hero {
  min-height: 100vh;
}
```

`100vh` means full screen height.

### vw

`vw` is relative to viewport width.

```css
.full-width {
  width: 100vw;
}
```

`100vw` means full screen width.

## 5. Practical unit usage

```txt
px  = fixed details like borders and icons
%   = responsive width based on parent
rem = font size and spacing
em  = component-relative spacing
vh  = full screen height sections
vw  = viewport width
```

## 6. What is the CSS box model?

In CSS, every HTML element is treated like a box.

The box model has four parts:

```txt
Content
Padding
Border
Margin
```

Visual:

```txt
Margin
  Border
    Padding
      Content
```

Example:

```css
.card {
  width: 300px;
  padding: 20px;
  border: 2px solid black;
  margin: 30px;
}
```

## 7. Content

Content is the actual text, image, video, or data inside the element.

```html
<p>This text is content.</p>
```

## 8. Padding

Padding is the space between the content and the border.

```css
.card {
  padding: 20px;
}
```

Use padding to create breathing space inside an element.

## 9. Border

Border is the line around the content and padding.

```css
.card {
  border: 1px solid #e5e7eb;
}
```

Border has width, style, and color.

```css
.card {
  border-width: 1px;
  border-style: solid;
  border-color: #e5e7eb;
}
```

Shortcut:

```css
.card {
  border: 1px solid #e5e7eb;
}
```

## 10. Border radius

`border-radius` creates rounded corners.

```css
.card {
  border-radius: 16px;
}
```

Circle avatar:

```css
.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
}
```

## 11. Margin

Margin is the space outside the border. It separates one element from another element.

```css
.card {
  margin-bottom: 24px;
}
```

Center block element:

```css
.container {
  max-width: 1200px;
  margin: 0 auto;
}
```

## 12. Margin and padding shorthand

```css
.box {
  margin: 10px;
}
```

All sides are `10px`.

```css
.box {
  margin: 10px 20px;
}
```

Top/bottom = `10px`, left/right = `20px`.

```css
.box {
  margin: 10px 20px 30px 40px;
}
```

Clockwise order:

```txt
top = 10px
right = 20px
bottom = 30px
left = 40px
```

Same shorthand works for padding.

## 13. Important: box-sizing

Default CSS uses:

```css
.box {
  box-sizing: content-box;
}
```

With `content-box`, width includes only the content. Padding and border are added extra.

Example:

```css
.box {
  width: 300px;
  padding: 20px;
  border: 2px solid black;
}
```

Actual total width:

```txt
300 + 20 + 20 + 2 + 2 = 344px
```

Best practice:

```css
* {
  box-sizing: border-box;
}
```

With `border-box`, width includes content + padding + border, which makes layouts easier to manage.

## 14. Interview answer

CSS colors can be written using named colors, HEX, RGB, RGBA, HSL, or CSS variables. Units define size. `px` is fixed, `%` is relative to the parent, `rem` is relative to the root font size, `em` is relative to the current element font size, and `vh`/`vw` are relative to viewport height and width.

The CSS box model explains how every element takes space on the page. It has content, padding, border, and margin. Content is the actual text or media. Padding is inside space between content and border. Border wraps the content and padding. Margin is outside space that separates elements.

## 15. Practice questions

1. What is the difference between HEX, RGB, RGBA, and HSL?
2. What is the difference between `px`, `%`, `rem`, `em`, `vh`, and `vw`?
3. What is the CSS box model?
4. What is the difference between margin and padding?
5. Why do we use `box-sizing: border-box`?
