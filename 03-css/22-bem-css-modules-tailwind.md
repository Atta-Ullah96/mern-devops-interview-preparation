# BEM, CSS Modules and Tailwind CSS

## 1. BEM

BEM is a CSS naming convention.

BEM stands for:

```txt
Block
Element
Modifier
```

It helps us write clean and predictable class names.

### BEM Example

HTML:

```html
<div class="card card--featured">
  <h2 class="card__title">Pro Plan</h2>
  <p class="card__description">Best for small teams.</p>
  <button class="card__button">Choose Plan</button>
</div>
```

CSS:

```css
.card {
  padding: 24px;
  border-radius: 16px;
}

.card__title {
  font-size: 24px;
}

.card__description {
  color: #6b7280;
}

.card__button {
  padding: 12px 18px;
}

.card--featured {
  border: 2px solid #2563eb;
}
```

Meaning:

```txt
card = Block
card__title = Element
card--featured = Modifier
```

### BEM Interview Answer

BEM is a CSS naming convention that stands for Block, Element, and Modifier. It helps write maintainable and readable CSS by making class names clear and predictable. It also reduces naming conflicts in large projects.

## 2. CSS Modules

CSS Modules are commonly used in React and Next.js to scope CSS to one component.

Normal CSS is global:

```css
.button {
  background-color: blue;
}
```

This can affect all `.button` classes in the app.

CSS Modules solve this problem by making class names locally scoped.

### CSS Module Example

File:

```txt
Button.module.css
```

```css
.button {
  background-color: #2563eb;
  color: white;
  padding: 12px 18px;
}
```

React component:

```jsx
import styles from "./Button.module.css";

function Button() {
  return <button className={styles.button}>Login</button>;
}
```

Behind the scenes, CSS Modules generate unique class names like:

```txt
Button_button__abc123
```

### CSS Modules Interview Answer

CSS Modules allow us to write CSS scoped to a specific component. The class names are locally scoped and compiled into unique names, so they do not conflict with styles in other components. They are very useful in React and Next.js projects.

## 3. Tailwind CSS

Tailwind CSS is a utility-first CSS framework.

Instead of writing custom CSS classes, we use utility classes directly in HTML or JSX.

Normal CSS:

```css
.btn {
  background-color: blue;
  color: white;
  padding: 12px 20px;
  border-radius: 8px;
}
```

Tailwind:

```html
<button class="bg-blue-600 text-white px-5 py-3 rounded-lg">
  Login
</button>
```

React:

```jsx
function Button() {
  return (
    <button className="bg-blue-600 text-white px-5 py-3 rounded-lg">
      Login
    </button>
  );
}
```

### Tailwind Responsive Example

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
  <div class="p-6 rounded-xl shadow">Card 1</div>
  <div class="p-6 rounded-xl shadow">Card 2</div>
  <div class="p-6 rounded-xl shadow">Card 3</div>
</div>
```

Meaning:

```txt
Mobile = 1 column
Tablet = 2 columns
Desktop = 3 columns
```

### Tailwind Interview Answer

Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS classes, we use small utility classes directly in HTML or JSX. It helps build UI faster, keeps spacing and colors consistent, and works very well with React and Next.js.

## BEM vs CSS Modules vs Tailwind

| Approach | Best For |
|---|---|
| BEM | Traditional CSS projects and clear naming |
| CSS Modules | React/Next.js component-scoped CSS |
| Tailwind | Fast utility-first UI development |
