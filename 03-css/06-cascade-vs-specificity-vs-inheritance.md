# Cascade vs Specificity vs Inheritance

These three concepts are connected, but they are not the same.

## Cascade

Cascade means the browser decides the final style when multiple CSS rules exist.

The cascade considers:

```txt
Importance
Specificity
Source order
Inheritance
```

Example:

```css
p {
  color: blue;
}

p {
  color: red;
}
```

Final color is `red` because both selectors have the same specificity, but the second rule comes later.

## Specificity

Specificity is the priority or weight of a selector.

Example:

```css
p {
  color: blue;
}

.text {
  color: green;
}
```

```html
<p class="text">Hello</p>
```

Final color is `green` because class selector has higher specificity than element selector.

## Inheritance

Inheritance means some CSS properties pass from parent to child automatically.

Example:

```css
body {
  color: black;
}
```

```html
<body>
  <p>Hello</p>
</body>
```

The paragraph inherits black color from body unless another rule overrides it.

## Combined example

HTML:

```html
<body>
  <div class="card">
    <p id="intro" class="text">Hello</p>
  </div>
</body>
```

CSS:

```css
body {
  color: black;
}

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

Final color is `red`.

Why?

```txt
body color inherited = black
p selector = blue
class selector = green
id selector = red
```

ID wins because it has the highest specificity among these rules.

## Simple difference

```txt
Cascade     = How browser chooses final style.
Specificity = Which selector is stronger.
Inheritance = Parent styles passing to child.
```

## Interview answer

> Cascade, specificity, and inheritance are part of how the browser calculates final CSS styles. Cascade is the overall process of deciding which rule applies. Specificity is the weight of a selector when multiple rules target the same element. Inheritance means some properties like color and font-family pass from parent elements to child elements automatically.

## What I learned

- Cascade is the full decision-making system.
- Specificity is selector priority.
- Inheritance passes some parent styles to children.
- A direct CSS rule can override inherited styles.
