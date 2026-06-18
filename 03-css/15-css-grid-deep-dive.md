# CSS Grid Deep Dive

## What is CSS Grid?

CSS Grid is a layout system used for **two-dimensional layouts**.

Simple meaning:

> Grid helps us create layouts with rows and columns together.

Flexbox handles one direction. Grid handles two directions.

```txt
Flexbox = row OR column
Grid    = rows AND columns
```

## Why CSS Grid is useful

Grid is useful when we need structured layouts like:

- Card grids
- Dashboards
- Image galleries
- Product listings
- Admin panels
- Full page layouts

## Basic Grid Example

HTML:

```html
<div class="grid">
  <div class="card">Card 1</div>
  <div class="card">Card 2</div>
  <div class="card">Card 3</div>
</div>
```

CSS:

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
```

This creates 3 equal columns.

## Grid Container and Grid Items

```html
<div class="grid">
  <div class="item">One</div>
  <div class="item">Two</div>
</div>
```

- `.grid` is the grid container.
- `.item` elements are grid items.

## grid-template-columns

This defines columns.

```css
.grid {
  grid-template-columns: 1fr 1fr 1fr;
}
```

This creates 3 equal columns.

Better version:

```css
.grid {
  grid-template-columns: repeat(3, 1fr);
}
```

## grid-template-rows

This defines rows.

```css
.grid {
  grid-template-rows: 100px 200px;
}
```

This creates two rows with different heights.

## What is `fr`?

`fr` means fraction of available space.

```css
.grid {
  grid-template-columns: 1fr 2fr;
}
```

Meaning:

```txt
First column = 1 part
Second column = 2 parts
```

Second column will be double the size of first column.

## repeat()

`repeat()` avoids writing the same value again and again.

```css
.grid {
  grid-template-columns: repeat(4, 1fr);
}
```

This means 4 equal columns.

## gap

`gap` creates space between rows and columns.

```css
.grid {
  display: grid;
  gap: 24px;
}
```

Separate gaps:

```css
.grid {
  row-gap: 20px;
  column-gap: 30px;
}
```

## minmax()

`minmax()` defines minimum and maximum size.

```css
.grid {
  grid-template-columns: repeat(3, minmax(200px, 1fr));
}
```

Each column will be at least `200px`, but can grow up to `1fr`.

## auto-fit with minmax

This is very useful for responsive layouts.

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 24px;
}
```

Meaning:

- Every card should be at least 250px.
- If there is space, cards expand.
- If there is not enough space, cards move to the next row.

This creates responsive cards without writing many media queries.

## auto-fit vs auto-fill

Both are used for responsive columns.

### auto-fit

`auto-fit` collapses empty tracks and lets existing items expand.

### auto-fill

`auto-fill` keeps empty tracks even if there are not enough items.

In most card layouts, `auto-fit` is easier and more common.

## grid-column

This controls how many columns an item spans.

```css
.featured-card {
  grid-column: span 2;
}
```

This item takes 2 columns.

## grid-row

```css
.tall-card {
  grid-row: span 2;
}
```

This item takes 2 rows.

## place-items

`place-items` is shorthand for aligning items horizontally and vertically.

```css
.grid {
  display: grid;
  place-items: center;
}
```

## Real dashboard layout

```css
.dashboard {
  display: grid;
  grid-template-columns: 240px 1fr;
  min-height: 100vh;
}
```

This creates:

- Sidebar: 240px
- Main content: remaining space

## Interview Answer

> CSS Grid is a two-dimensional layout system used to create rows and columns. It is useful for page layouts, dashboards, galleries, and card grids. Common Grid properties include `display: grid`, `grid-template-columns`, `grid-template-rows`, `gap`, `repeat`, `fr`, `minmax`, `auto-fit`, and `auto-fill`.

## Common Interview Questions

1. What is CSS Grid?
2. What is the difference between Grid and Flexbox?
3. What does `fr` mean?
4. What does `repeat(3, 1fr)` mean?
5. What does `minmax(250px, 1fr)` mean?
6. What is the use of `auto-fit`?
7. How do you create a responsive card grid?

## What I Learned

- Grid is best for two-dimensional layouts.
- `fr` divides available space into fractions.
- `repeat()` makes grid code cleaner.
- `minmax()` helps create flexible layouts.
- `auto-fit` and `minmax()` are very useful for responsive card layouts.
