# CSS Specificity

## What is specificity?

Specificity means the priority or weight of a CSS selector.

When multiple CSS rules target the same element, specificity decides which rule will apply.

Example:

```html
<p id="intro" class="text">Hello</p>
```

```css
p {
  color: blue;
}

.text {
  color: green;
}

#intro {
  color: red;
}
```

Final color will be `red` because ID selector has higher specificity than class and element selectors.

## Specificity priority order

```txt
Inline style > ID selector > Class selector > Element selector > Universal selector
```

## Specificity score

A simple way to remember specificity:

```txt
Inline style = 1000
ID           = 100
Class        = 10
Element      = 1
Universal    = 0
```

Example:

```css
p {
  color: blue;
}
```

Specificity = 1

```css
.text {
  color: green;
}
```

Specificity = 10

```css
#intro {
  color: red;
}
```

Specificity = 100

```html
<p id="intro" class="text" style="color: orange;">Hello</p>
```

Inline style wins, so final color is `orange`.

## Deep specificity example

HTML:

```html
<div class="card">
  <p class="text">Hello</p>
</div>
```

CSS:

```css
p {
  color: blue;
}

.text {
  color: green;
}

.card .text {
  color: red;
}
```

Final color will be `red`.

Why?

```txt
p            = 1
.text        = 10
.card .text  = 20
```

`.card .text` wins.

## What if specificity is same?

If specificity is the same, the later rule wins.

Example:

```css
.text {
  color: blue;
}

.text {
  color: red;
}
```

Final color will be `red` because both selectors have the same specificity, but the red rule comes later.

## What is `!important`?

`!important` forces a CSS rule to win over normal rules.

Example:

```css
.text {
  color: blue !important;
}

#intro {
  color: red;
}
```

Final color will be `blue` because `!important` overrides normal specificity.

## Why avoid `!important`?

Avoid `!important` because:

```txt
It makes CSS hard to debug.
It breaks the normal cascade.
It creates maintenance problems.
It can cause more !important usage later.
```

## Interview answer

> Specificity means the priority or weight of a CSS selector. When multiple CSS rules target the same element, specificity decides which style will apply. Inline styles have the highest priority, followed by ID selectors, class selectors, element selectors, and universal selectors. If specificity is the same, the CSS rule that comes later wins. `!important` can override normal specificity, but it should be avoided unless necessary.

## What I learned

- Specificity decides which CSS rule wins.
- Inline styles have the highest priority.
- ID selectors are stronger than class selectors.
- Class selectors are stronger than element selectors.
- If specificity is the same, the later rule wins.
- Avoid `!important` in normal CSS.
