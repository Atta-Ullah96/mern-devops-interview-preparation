# Advanced CSS Interview Answers

## 1. What is the difference between pseudo classes and pseudo elements?

Pseudo classes style an element based on its state or position, such as `:hover`, `:focus`, `:active`, `:disabled`, and `:nth-child`.

Pseudo elements style a specific part of an element or insert visual content, such as `::before`, `::after`, `::first-letter`, and `::placeholder`.

## 2. What is the difference between transition, transform, and animation?

A transition makes a CSS property change smoothly over time. A transform visually moves, scales, rotates, or skews an element without affecting normal layout. An animation uses `@keyframes` to create complex or repeated movement.

## 3. Why is transform better for animations than margin or top?

`transform` is usually better because it does not force the browser to recalculate the full layout. Properties like margin, top, width, and height can trigger layout recalculation and make animations less smooth.

## 4. What is BEM?

BEM stands for Block, Element, and Modifier. It is a CSS naming convention that makes class names clear and maintainable.

## 5. What are CSS Modules?

CSS Modules allow us to write CSS scoped to a specific component. They are useful in React and Next.js because they prevent global class name conflicts.

## 6. What is Tailwind CSS?

Tailwind CSS is a utility-first CSS framework. Instead of writing custom CSS classes, we use utility classes directly in HTML or JSX.

## 7. What is layout shift?

Layout shift happens when content moves unexpectedly after page load. Example: an image loads late and pushes a button down.

## 8. How can we reduce layout shift?

We can reduce layout shift by defining image width and height, reserving space for dynamic content, using proper skeleton loaders, and avoiding inserting content above existing content.

## 9. What is mobile-first design?

Mobile-first design means writing default CSS for mobile screens first, then using `min-width` media queries for larger screens.

## 10. How can CSS affect performance?

CSS can affect performance through large unused CSS files, complex selectors, expensive animations, and layout shifts. For better performance, we should remove unused CSS, minify CSS, avoid complex selectors, and animate `transform` and `opacity` instead of layout properties.
