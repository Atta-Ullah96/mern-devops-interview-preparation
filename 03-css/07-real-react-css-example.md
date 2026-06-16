# Real React CSS Example

In React, we use `className` instead of `class`.

## Why React uses className

In JavaScript, `class` is a reserved keyword.

So in JSX, we write:

```jsx
<button className="btn-primary">Login</button>
```

React converts it to normal HTML:

```html
<button class="btn-primary">Login</button>
```

## Example React component

```jsx
function LoginButton() {
  return <button className="btn-primary">Login</button>;
}

export default LoginButton;
```

## CSS

```css
.btn-primary {
  background-color: blue;
  color: white;
  padding: 12px 20px;
  border-radius: 8px;
  border: none;
  cursor: pointer;
}

.btn-primary:hover {
  background-color: darkblue;
}
```

## Why class selector is good in React

Class selectors are good because:

```txt
They are reusable.
They keep JSX clean.
They are easier to maintain.
They work with hover/focus states.
They avoid repeating inline CSS.
```

## Inline style in React

React also supports inline styles:

```jsx
function Heading() {
  return <h1 style={{ color: "red", fontSize: "40px" }}>Hello</h1>;
}
```

But inline style is usually not preferred for normal styling because it is less reusable and does not support pseudo-classes like `:hover`.

## Interview point

> In React, CSS can be applied using normal CSS files, CSS modules, inline styles, styled-components, Tailwind CSS, or other styling methods. For normal reusable styles, class-based styling is usually cleaner than inline CSS.
