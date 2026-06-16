# CSS Cheat Sheet

## CSS meaning

```txt
CSS = Cascading Style Sheets
```

## HTML, CSS, JS

```txt
HTML       = structure
CSS        = design
JavaScript = behavior
```

## CSS types

```txt
Inline CSS   = style attribute
Internal CSS = style tag
External CSS = separate .css file
```

## Inline CSS

```html
<h1 style="color: red;">Hello</h1>
```

## Internal CSS

```html
<style>
  h1 {
    color: blue;
  }
</style>
```

## External CSS

```html
<link rel="stylesheet" href="style.css" />
```

## Selectors

```css
* {}                /* universal */
p {}                /* element */
.card {}            /* class */
#title {}           /* id */
input[type="email"] {} /* attribute */
button:hover {}     /* pseudo-class */
p::first-letter {}  /* pseudo-element */
```

## Specificity order

```txt
Inline style > ID > Class > Element > Universal
```

## Specificity score

```txt
Inline = 1000
ID     = 100
Class  = 10
Element = 1
Universal = 0
```

## Inherited properties

```txt
color
font-family
font-size
font-weight
line-height
text-align
```

## Non-inherited properties

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

## Cascade vs specificity vs inheritance

```txt
Cascade     = browser decides final style
Specificity = selector priority
Inheritance = parent style passes to child
```

## React CSS

```jsx
<button className="btn-primary">Login</button>
```

```css
.btn-primary {
  background-color: blue;
  color: white;
}
```
