# Advanced CSS Cheat Sheet

## Pseudo Classes

```css
button:hover {}
input:focus {}
button:active {}
button:disabled {}
li:first-child {}
li:last-child {}
li:nth-child(2) {}
```

## Pseudo Elements

```css
.title::before {}
.title::after {}
p::first-letter {}
p::first-line {}
input::placeholder {}
```

## Transition

```css
.button {
  transition: background-color 0.3s ease;
}
```

Better:

```css
.card {
  transition: transform 0.3s ease, opacity 0.3s ease;
}
```

Avoid:

```css
.card {
  transition: all 0.3s ease;
}
```

## Transform

```css
transform: translateX(20px);
transform: translateY(-10px);
transform: scale(1.1);
transform: rotate(10deg);
```

## Animation

```css
@keyframes fadeIn {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}

.box {
  animation: fadeIn 0.5s ease forwards;
}
```

## BEM

```html
<div class="card card--featured">
  <h2 class="card__title">Title</h2>
</div>
```

```txt
card = Block
card__title = Element
card--featured = Modifier
```

## CSS Modules

```txt
Button.module.css
```

```jsx
import styles from "./Button.module.css";

<button className={styles.button}>Click</button>
```

## Tailwind

```html
<button class="bg-blue-600 text-white px-5 py-3 rounded-lg">
  Login
</button>
```

Responsive:

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
```

## CSS Performance

Prefer animating:

```txt
transform
opacity
```

Avoid animating:

```txt
width
height
top
left
margin
padding
```

## Layout Shift Fixes

```html
<img src="hero.jpg" width="1200" height="600" alt="Hero image" />
```

```css
.image-wrapper {
  aspect-ratio: 16 / 9;
}
```

## Mobile-First

```css
.container {
  display: block;
}

@media (min-width: 768px) {
  .container {
    display: flex;
  }
}
```
