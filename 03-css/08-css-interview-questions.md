# CSS Interview Questions

## Basic questions

1. What is CSS?
2. Why was CSS created?
3. What problem did CSS solve?
4. What does Cascading mean in CSS?
5. What is the difference between HTML and CSS?

## Inline, internal, external CSS

6. What is inline CSS?
7. What is internal CSS?
8. What is external CSS?
9. Which CSS method is best for large projects and why?
10. What are the disadvantages of inline CSS?

## Selectors

11. What are CSS selectors?
12. What is an element selector?
13. What is a class selector?
14. What is an ID selector?
15. What is the difference between class and ID?
16. What is a universal selector?
17. What is an attribute selector?
18. What is a pseudo-class?
19. What is a pseudo-element?
20. What is the difference between `:hover` and `::before`?

## Specificity

21. What is specificity in CSS?
22. Which has more specificity: class or ID?
23. What is the specificity order?
24. What happens if two selectors have the same specificity?
25. What is `!important`?
26. Why should we avoid `!important`?

## Inheritance

27. What is inheritance in CSS?
28. Which properties are usually inherited?
29. Which properties are usually not inherited?
30. How can we force inheritance?

## Practical questions

31. Why should we avoid using tables for layout?
32. Why is external CSS cacheable?
33. Why is CSS important in React apps?
34. Why does React use `className` instead of `class`?
35. How do you debug CSS issues?

## Strong answer to memorize

> CSS stands for Cascading Style Sheets. It was created to separate webpage structure from design. HTML should handle content and structure, while CSS should handle styling and layout. This makes code cleaner, easier to maintain, and reusable across multiple pages.
>
> CSS can be added in three ways: inline, internal, and external. Inline CSS is written inside an element using the `style` attribute. Internal CSS is written inside the `<style>` tag in the HTML file. External CSS is written in a separate `.css` file and linked using the `<link>` tag. In real projects, external CSS is preferred because it is cleaner, reusable, and maintainable.
>
> CSS selectors are used to target HTML elements. Common selectors include element selectors, class selectors, ID selectors, universal selectors, attribute selectors, pseudo-classes, and pseudo-elements. Specificity decides which CSS rule wins when multiple rules target the same element. Inline style has the highest priority, then ID, then class, then element, then universal selector. Inheritance means some styles like color and font-family pass from parent to child elements automatically.
