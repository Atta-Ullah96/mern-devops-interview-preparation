# Flexbox Deep Dive

## What is Flexbox?

Flexbox means **Flexible Box Layout**.

Flexbox is a CSS layout system used to arrange elements in **one direction**:

- Row
- Column

Simple meaning:

> Flexbox is used when we want to align, distribute, and space items easily in a row or column.

## Why Flexbox was created

Before Flexbox, developers used floats, tables, and manual margins for layout. This made alignment difficult.

Example problems before Flexbox:

- Centering an item vertically was difficult.
- Creating equal-height columns was difficult.
- Aligning navbar items was difficult.
- Spacing items evenly was difficult.
- Responsive row layouts were harder.

Flexbox solved these layout problems.

## Basic Flexbox Example

```html
<div class="container">
  <div class="box">Box 1</div>
  <div class="box">Box 2</div>
  <div class="box">Box 3</div>
</div>
```

```css
.container {
  display: flex;
  gap: 20px;
}

.box {
  padding: 20px;
  background-color: #2563eb;
  color: white;
}
```

When we write `display: flex`, the direct children become flex items.

## Flex Container and Flex Items

```html
<div class="container">
  <div class="item">One</div>
  <div class="item">Two</div>
</div>
```

- `.container` is the flex container.
- `.item` elements are flex items.

Flexbox properties are divided into two parts:

### Container properties

- `display: flex`
- `flex-direction`
- `justify-content`
- `align-items`
- `gap`
- `flex-wrap`
- `align-content`

### Item properties

- `flex`
- `flex-grow`
- `flex-shrink`
- `flex-basis`
- `align-self`
- `order`

## Main Axis and Cross Axis

Flexbox has two axes:

- Main axis
- Cross axis

If `flex-direction: row`:

```txt
Main axis  = horizontal
Cross axis = vertical
```

If `flex-direction: column`:

```txt
Main axis  = vertical
Cross axis = horizontal
```

This is important because:

- `justify-content` works on the main axis.
- `align-items` works on the cross axis.

## flex-direction

`flex-direction` controls the direction of flex items.

```css
.container {
  display: flex;
  flex-direction: row;
}
```

Common values:

```txt
row
row-reverse
column
column-reverse
```

### row

```css
.container {
  flex-direction: row;
}
```

Items go left to right.

### column

```css
.container {
  flex-direction: column;
}
```

Items go top to bottom.

## justify-content

`justify-content` aligns items on the main axis.

```css
.container {
  display: flex;
  justify-content: center;
}
```

Common values:

```txt
flex-start
center
flex-end
space-between
space-around
space-evenly
```

Example navbar:

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

This places the logo on one side and links on the other side.

## align-items

`align-items` aligns items on the cross axis.

```css
.container {
  display: flex;
  align-items: center;
}
```

Common values:

```txt
stretch
center
flex-start
flex-end
baseline
```

## Centering with Flexbox

```css
.parent {
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

This centers the child horizontally and vertically.

## gap

`gap` creates space between flex items.

```css
.container {
  display: flex;
  gap: 20px;
}
```

This is cleaner than adding margin to each item.

## flex-wrap

By default, flex items stay on one line.

```css
.container {
  display: flex;
  flex-wrap: wrap;
}
```

If items do not fit, they move to the next line.

## flex: 1

```css
.item {
  flex: 1;
}
```

This means items share available space equally.

Example:

```css
.cards {
  display: flex;
  gap: 20px;
}

.card {
  flex: 1;
}
```

All cards will take equal width.

## flex-grow, flex-shrink, flex-basis

`flex` is shorthand for:

```txt
flex-grow
flex-shrink
flex-basis
```

Example:

```css
.item {
  flex: 1 1 250px;
}
```

Meaning:

- `1` = item can grow
- `1` = item can shrink
- `250px` = starting size

## align-self

`align-self` overrides `align-items` for one item.

```css
.special-item {
  align-self: flex-end;
}
```

## order

`order` changes visual order.

```css
.item-1 {
  order: 2;
}

.item-2 {
  order: 1;
}
```

Use carefully because it can affect accessibility and keyboard flow.

## Real use cases

Use Flexbox for:

- Navbar
- Button with icon
- Centering content
- Form row
- Sidebar + content simple layout
- Card footer alignment
- User profile row

## Interview Answer

> Flexbox is a CSS layout system used for one-dimensional layouts, either row or column. It helps align and distribute items easily. In Flexbox, `justify-content` works on the main axis and `align-items` works on the cross axis. Common Flexbox properties include `display: flex`, `flex-direction`, `justify-content`, `align-items`, `gap`, `flex-wrap`, and `flex`.

## Common Interview Questions

1. What is Flexbox?
2. What is the difference between main axis and cross axis?
3. What is the difference between `justify-content` and `align-items`?
4. What is `flex-wrap`?
5. What does `flex: 1` mean?
6. How do you center a div using Flexbox?
7. When should we use Flexbox instead of Grid?

## What I Learned

- Flexbox is best for one-dimensional layouts.
- `justify-content` works on the main axis.
- `align-items` works on the cross axis.
- `gap` is better than manually adding margins between flex items.
- Flexbox is great for navbars, alignment, and small component layouts.
