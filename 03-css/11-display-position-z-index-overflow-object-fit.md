# CSS Display, Position, Z-index, Overflow and Object-fit

## 1. Display property

The `display` property controls how an element behaves in the layout.

Common display values:

```txt
block
inline
inline-block
none
flex
grid
```

## 2. display: block

Block elements take the full available width and start on a new line.

```css
.box {
  display: block;
}
```

Common block elements:

```txt
div
p
h1
section
main
article
```

Example:

```html
<div>Box 1</div>
<div>Box 2</div>
```

Output behavior:

```txt
Box 1
Box 2
```

## 3. display: inline

Inline elements take only the width they need and stay on the same line.

```css
.text {
  display: inline;
}
```

Common inline elements:

```txt
span
a
strong
em
```

Example:

```html
<span>Hello</span>
<span>World</span>
```

Output behavior:

```txt
Hello World
```

Important:

```txt
width and height usually do not work properly on inline elements
```

## 4. display: inline-block

Inline-block behaves like inline because it stays on the same line, but it also behaves like block because width, height, padding, and margin work properly.

```css
.button-link {
  display: inline-block;
  width: 160px;
  padding: 12px 20px;
}
```

Use inline-block for:

```txt
buttons
badges
links styled as buttons
small cards
```

## 5. display: none

`display: none` hides the element and removes it from the layout.

```css
.modal {
  display: none;
}
```

Important difference:

```txt
display: none       = element hidden and space removed
visibility: hidden  = element hidden but space remains
```

## 6. display: flex

Flex is used for one-dimensional layouts: row or column.

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

Use flex for:

```txt
navbar
button with icon
centering content
row/column alignment
```

## 7. display: grid

Grid is used for two-dimensional layouts: rows and columns together.

```css
.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
```

Use grid for:

```txt
card layouts
dashboards
image galleries
page layouts
```

## 8. Position property

The `position` property controls how an element is placed on the page.

Common values:

```txt
static
relative
absolute
fixed
sticky
```

## 9. position: static

Static is the default value.

```css
.box {
  position: static;
}
```

Static elements follow the normal document flow.

Important:

```txt
top, right, bottom, and left do not work on static elements
```

## 10. position: relative

Relative keeps the element in normal flow, but allows visual movement using top, left, right, and bottom.

```css
.box {
  position: relative;
  top: 20px;
  left: 10px;
}
```

Important:

```txt
The original space of the element is still reserved.
```

Common use:

```css
.parent {
  position: relative;
}
```

This allows an absolute child to position itself inside the parent.

## 11. position: absolute

Absolute removes the element from normal flow and positions it relative to the nearest positioned parent.

```css
.card {
  position: relative;
}

.badge {
  position: absolute;
  top: 12px;
  right: 12px;
}
```

If no positioned parent exists, absolute usually positions relative to the page/body.

Use absolute for:

```txt
badges
icons
tooltips
dropdowns
overlays inside cards
```

## 12. position: fixed

Fixed positions the element relative to the viewport/screen. It stays fixed when the user scrolls.

```css
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}
```

Use fixed for:

```txt
fixed navbar
chat button
floating WhatsApp button
modal overlay
```

## 13. position: sticky

Sticky is a mix of relative and fixed. It behaves normally until it reaches a scroll point, then it sticks.

```css
.header {
  position: sticky;
  top: 0;
}
```

Use sticky for:

```txt
sticky navbar
sticky sidebar
sticky table header
```

Important:

```txt
Sticky needs a top, left, right, or bottom value.
```

## 14. Z-index

`z-index` controls stacking order, meaning which element appears above another.

```css
.modal {
  position: fixed;
  z-index: 1000;
}

.dropdown {
  position: absolute;
  z-index: 100;
}
```

Higher z-index appears above lower z-index.

Important:

```txt
z-index usually works on positioned elements like relative, absolute, fixed, and sticky.
```

Common issue:

```txt
Dropdown is behind another element
Modal is not above overlay
Tooltip is hidden behind card
```

Possible reasons:

```txt
z-index is too low
parent has overflow hidden
parent created stacking context
element is not positioned
```

Some properties can create stacking context:

```txt
position + z-index
transform
opacity less than 1
filter
isolation
```

## 15. Overflow

Overflow controls what happens when content is bigger than its container.

```css
.box {
  width: 200px;
  height: 100px;
  overflow: hidden;
}
```

## 16. overflow: visible

Default value. Extra content is visible outside the box.

```css
.box {
  overflow: visible;
}
```

## 17. overflow: hidden

Extra content is clipped/hidden.

```css
.box {
  overflow: hidden;
}
```

Use it for:

```txt
hiding extra content
rounded card images
preventing content from spilling outside
```

## 18. overflow: scroll

Scrollbars are always shown.

```css
.box {
  overflow: scroll;
}
```

## 19. overflow: auto

Scrollbars appear only when needed.

```css
.sidebar {
  height: 100vh;
  overflow-y: auto;
}
```

This is usually better than `scroll` for real UI.

## 20. overflow-x and overflow-y

```css
.box {
  overflow-x: hidden;
  overflow-y: auto;
}
```

Use this when you want to control horizontal and vertical overflow separately.

## 21. Text truncation with overflow

```css
.title {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

This creates:

```txt
This is a very long...
```

## 22. Object-fit

`object-fit` controls how an image or video fits inside its container.

Example:

```css
.card-image {
  width: 100%;
  height: 220px;
  object-fit: cover;
}
```

## 23. object-fit: cover

Cover fills the container while keeping the image aspect ratio. It may crop extra parts.

```css
.image {
  width: 300px;
  height: 200px;
  object-fit: cover;
}
```

Use cover for:

```txt
card images
avatars
thumbnails
hero images
```

## 24. object-fit: contain

Contain shows the full image while keeping aspect ratio. It may leave empty space.

```css
.logo {
  width: 300px;
  height: 200px;
  object-fit: contain;
}
```

Use contain for:

```txt
logos
product images
images where cropping is not allowed
```

## 25. object-fit: fill

Fill stretches the image to fit the container. It can distort the image, so usually avoid it.

```css
.image {
  object-fit: fill;
}
```

## 26. Interview answer

The display property controls how elements behave in layout. Block elements take full width and start on a new line. Inline elements take only required width and stay on the same line. Inline-block stays on the same line but supports width and height. Display none hides the element and removes its space. Flex is used for one-dimensional layouts, and Grid is used for two-dimensional layouts.

The position property controls element placement. Static is default and follows normal flow. Relative keeps the element in normal flow but allows visual movement. Absolute removes the element from normal flow and positions relative to the nearest positioned parent. Fixed positions relative to the viewport and stays during scroll. Sticky behaves normally until a scroll point, then sticks.

Z-index controls stacking order. Overflow controls what happens when content is larger than the container. Object-fit controls how images or videos fit inside a fixed-size container.

## 27. Practice questions

1. What is the difference between block, inline, inline-block, none, flex, and grid?
2. What is the difference between static, relative, absolute, fixed, and sticky?
3. Why does z-index sometimes not work?
4. What is the difference between overflow hidden, scroll, and auto?
5. What is the difference between object-fit cover and contain?
