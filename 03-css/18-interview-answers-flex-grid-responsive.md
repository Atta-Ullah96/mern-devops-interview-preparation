# Interview Answers: Flexbox, Grid, Responsive Design and Media Queries

## Question 1: What is Flexbox?

Flexbox is a CSS layout system used for one-dimensional layouts, either row or column. It helps align, distribute, and space items easily. Common Flexbox properties are `display: flex`, `flex-direction`, `justify-content`, `align-items`, `gap`, `flex-wrap`, and `flex`.

## Question 2: What is the difference between justify-content and align-items?

`justify-content` aligns items on the main axis, while `align-items` aligns items on the cross axis.

If `flex-direction` is row:

```txt
justify-content = horizontal alignment
align-items     = vertical alignment
```

If `flex-direction` is column:

```txt
justify-content = vertical alignment
align-items     = horizontal alignment
```

## Question 3: How do you center a div using Flexbox?

```css
.parent {
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

This centers the child horizontally and vertically.

## Question 4: What is CSS Grid?

CSS Grid is a two-dimensional layout system used to create rows and columns. It is useful for card grids, dashboards, page layouts, image galleries, and product listings.

## Question 5: What is the difference between Flexbox and Grid?

Flexbox is one-dimensional and works with row or column. Grid is two-dimensional and works with rows and columns together. Flexbox is better for alignment, navbars, and buttons. Grid is better for full layouts, dashboards, galleries, and card grids.

## Question 6: What does `fr` mean in CSS Grid?

`fr` means fraction of available space.

```css
grid-template-columns: 1fr 2fr;
```

This means the second column will take twice as much space as the first column.

## Question 7: What is responsive design?

Responsive design means creating websites that look good and work well on different screen sizes, such as mobile, tablet, laptop, and desktop. It helps avoid broken layouts, horizontal scroll, unreadable text, and small buttons on mobile.

## Question 8: What are media queries?

Media queries allow us to apply CSS only when a condition is true, such as when the screen width is greater than or less than a specific size.

Example:

```css
@media (min-width: 768px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

## Question 9: What is mobile-first design?

Mobile-first design means writing CSS for small screens first, then adding styles for larger screens using `min-width` media queries.

Example:

```css
.card-grid {
  grid-template-columns: 1fr;
}

@media (min-width: 768px) {
  .card-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

## Question 10: Why is mobile-first design important?

Mobile-first design is important because many users browse websites on mobile devices. It keeps CSS cleaner, improves performance, and helps us build layouts that scale naturally from small screens to large screens.

## Question 11: How can we create a responsive card grid?

Using media queries:

```css
.cards {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
}

@media (min-width: 768px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .cards {
    grid-template-columns: repeat(3, 1fr);
  }
}
```

Using `auto-fit` and `minmax`:

```css
.cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 24px;
}
```

## Strong Combined Interview Answer

CSS Flexbox is used for one-dimensional layouts, either row or column. It is useful for alignment, navbars, buttons, and small component layouts. CSS Grid is used for two-dimensional layouts with rows and columns, such as card grids, dashboards, galleries, and page structures.

Responsive design means building websites that work well on mobile, tablet, laptop, and desktop screens. We achieve this using relative units, Flexbox, Grid, responsive images, and media queries. Media queries allow us to apply CSS based on screen size. A mobile-first approach means writing CSS for small screens first, then adding larger screen styles with `min-width` media queries.
