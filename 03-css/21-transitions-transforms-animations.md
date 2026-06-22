# Transitions, Transforms and Animations in CSS

## 1. Transitions

Transitions make CSS property changes smooth.

Without transition:

```css
button:hover {
  background-color: black;
}
```

The color changes instantly.

With transition:

```css
button {
  background-color: blue;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: black;
}
```

Now the color changes smoothly.

### Transition Syntax

```css
transition: property duration timing-function delay;
```

Example:

```css
.card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
```

Avoid this in large projects:

```css
transition: all 0.3s ease;
```

Better:

```css
transition: transform 0.3s ease, opacity 0.3s ease;
```

Because `transition: all` may animate unnecessary properties and hurt performance.

## 2. Transforms

Transform changes how an element looks visually without changing normal document layout.

Common transforms:

```css
transform: translateX(20px);
transform: translateY(-10px);
transform: scale(1.1);
transform: rotate(10deg);
```

### Translate

```css
.card:hover {
  transform: translateY(-6px);
}
```

### Scale

```css
.card:hover {
  transform: scale(1.03);
}
```

### Rotate

```css
.icon {
  transform: rotate(45deg);
}
```

### Why Transform Is Good for Performance

Animating `transform` is usually smoother than animating layout properties.

Good:

```css
.card:hover {
  transform: translateY(-10px);
}
```

Avoid:

```css
.card:hover {
  margin-top: -10px;
}
```

Because changing margin can trigger layout recalculation.

## 3. Animations

Animations are used for complex or repeated movement.

Transitions usually need a trigger like hover. Animations can run automatically.

### Basic Animation

```css
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(12px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.card {
  animation: fadeIn 0.5s ease forwards;
}
```

### Loader Example

```css
@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}

.loader {
  width: 40px;
  height: 40px;
  border: 4px solid #e5e7eb;
  border-top-color: #2563eb;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}
```

## Transition vs Transform vs Animation

| Topic | Meaning |
|---|---|
| Transition | Smoothly changes a property over time |
| Transform | Visually moves, scales, rotates, or skews an element |
| Animation | Uses keyframes for automatic or repeated movement |

## Interview Answer

Transitions make CSS changes smooth over time. Transform visually moves, scales, rotates, or skews an element without affecting layout flow. Animations use `@keyframes` to create complex or repeated movement. For performance, it is better to animate `transform` and `opacity` instead of layout properties like width, height, top, left, margin, or padding.
