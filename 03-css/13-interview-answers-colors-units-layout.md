# Interview Answers: CSS Colors, Units, Box Model, Display and Position

## Question 1: What is the difference between px, %, rem, em, vh, and vw?

`px` is a fixed unit. `%` is relative to the parent element. `rem` is relative to the root HTML font size, usually 16px by default. `em` is relative to the current element's font size, and if it is not set, it depends on the inherited parent font size. `vh` is relative to viewport height, and `vw` is relative to viewport width.

## Question 2: Explain the CSS box model.

In CSS, every HTML element is treated like a box. The box model has four parts: content, padding, border, and margin. Content is the actual text, image, or data inside the element. Padding is the space between the content and the border. Border is the line around the content and padding. Margin is the space outside the border that separates the element from other elements.

## Question 3: What is the difference between display block, inline, inline-block, none, flex, and grid?

The display property controls how an element behaves in layout. Block elements take full available width and start on a new line. Inline elements take only the required width and stay on the same line, but width and height usually do not work properly. Inline-block stays on the same line like inline, but allows width, height, padding, and margin like block. Display none hides the element and removes it from the layout. Flex is used for one-dimensional layouts like rows or columns. Grid is used for two-dimensional layouts with rows and columns.

## Question 4: Explain position static, relative, absolute, fixed, and sticky.

Static is the default position and follows normal document flow. Top, right, bottom, and left do not work on static elements. Relative keeps the element in normal flow but allows visual movement using top, left, right, or bottom. Absolute removes the element from normal flow and positions it relative to the nearest positioned parent. Fixed positions the element relative to the viewport, so it stays in the same place while scrolling. Sticky behaves like a normal element until a scroll point, then it sticks.

## Question 5: What is the difference between overflow hidden, auto, and scroll? Why do we use object-fit cover?

`overflow: hidden` clips extra content that goes outside the container. `overflow: scroll` always shows scrollbars. `overflow: auto` shows scrollbars only when content is larger than the container. `object-fit: cover` is used for images or videos to fill a fixed-size container while keeping the aspect ratio. It may crop the image, but it prevents stretching and keeps card images looking clean.
