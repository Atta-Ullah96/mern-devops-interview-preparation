# Flexbox vs Grid

## Main Difference

Flexbox and Grid are both CSS layout systems, but they solve different problems.

Simple rule:

```txt
Flexbox = one-dimensional layout
Grid    = two-dimensional layout
```

## Flexbox

Flexbox works in one direction at a time.

It handles:

- Row
- Column

Use Flexbox for alignment and smaller component layouts.

Examples:

- Navbar
- Button with icon
- User profile row
- Centering content
- Form row
- Card footer

Example:

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

## Grid

Grid works with rows and columns together.

Use Grid for full layout structure.

Examples:

- Card grid
- Dashboard
- Image gallery
- Product listing
- Admin layout
- Page sections

Example:

```css
.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
```

## Comparison Table

| Flexbox | Grid |
|---|---|
| One-dimensional | Two-dimensional |
| Row or column | Rows and columns |
| Best for alignment | Best for full layouts |
| Content-first | Layout-first |
| Navbar, buttons, form rows | Cards, dashboards, galleries |

## Content-first vs Layout-first

### Flexbox is content-first

Flexbox lets content decide how much space it needs and then aligns it.

Good for:

```txt
Logo + nav links
Icon + text button
Profile image + user details
```

### Grid is layout-first

Grid lets us define a layout structure first, then place items inside.

Good for:

```txt
3-column card layout
Sidebar + main content
Dashboard widgets
```

## Can we use both together?

Yes. In real projects, we often use both.

Example:

- Grid for page/card layout
- Flexbox inside each card for alignment

```css
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 24px;
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

## Practical rule

Use this rule in interviews:

```txt
Use Flexbox for alignment.
Use Grid for layouts.
```

## Interview Answer

> Flexbox is used for one-dimensional layouts, either row or column. Grid is used for two-dimensional layouts with rows and columns. I use Flexbox for alignment, navbars, buttons, and small component layouts. I use Grid for card layouts, dashboards, galleries, and page structure. In real projects, we often use both together: Grid for the main layout and Flexbox inside components.

## Common Interview Questions

1. What is the difference between Flexbox and Grid?
2. When should we use Flexbox?
3. When should we use Grid?
4. Can Flexbox and Grid be used together?
5. Why is Grid better for dashboards?
6. Why is Flexbox better for navbars?

## What I Learned

- Flexbox is one-dimensional.
- Grid is two-dimensional.
- Flexbox is best for alignment.
- Grid is best for layouts.
- Real projects commonly use both together.
