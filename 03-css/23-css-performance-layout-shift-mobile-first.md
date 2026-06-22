# CSS Performance, Layout Shift and Mobile-First Design

## 1. CSS Performance

CSS performance means writing styles that load and render efficiently.

Bad CSS can cause:

- Slow rendering
- Large CSS files
- Unused CSS
- Janky animations
- Layout shifts
- Poor mobile performance

## Remove Unused CSS

Large unused CSS slows down page loading.

In Tailwind, production build can remove unused classes if configured correctly.

## Avoid Expensive Animations

Good properties to animate:

```txt
transform
opacity
```

Avoid animating:

```txt
width
height
top
left
margin
padding
```

Because these properties can trigger layout recalculation.

Good:

```css
.card {
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-6px);
}
```

Bad:

```css
.card:hover {
  margin-top: -6px;
}
```

## Avoid Very Complex Selectors

Bad:

```css
body .app .main .section .card ul li a span {
  color: red;
}
```

Better:

```css
.card-link {
  color: red;
}
```

## CSS Performance Interview Answer

CSS performance means writing styles that load and render efficiently. We should remove unused CSS, avoid very complex selectors, minify production CSS, use responsive images, and prefer animating transform and opacity instead of layout properties like width, height, margin, or top.

---

# 2. Layout Shift

Layout shift means page content moves unexpectedly after loading.

Example:

```txt
User is about to click a button.
An image loads above it.
Button moves down.
User clicks wrong place.
```

This is bad user experience.

## Common Causes of Layout Shift

- Images without width and height
- Ads or banners loaded late
- Fonts loading late
- Dynamic content inserted above existing content
- Skeleton loaders with wrong size

## Image Layout Shift Problem

Bad:

```html
<img src="hero.jpg" alt="Hero image" />
```

Better:

```html
<img src="hero.jpg" width="1200" height="600" alt="Hero image" />
```

Now browser can reserve space.

## CSS Fix Using Aspect Ratio

```css
.image-wrapper {
  width: 100%;
  aspect-ratio: 16 / 9;
  overflow: hidden;
}

.image-wrapper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

## Layout Shift Interview Answer

Layout shift happens when elements move unexpectedly after page load. It usually happens because images, ads, fonts, or dynamic content load late without reserved space. To reduce layout shift, we should define image dimensions, reserve space for dynamic content, use proper skeleton loaders, and avoid inserting content above existing content.

---

# 3. Mobile-First Design

Mobile-first means writing CSS for mobile screens first, then adding styles for larger screens.

Bad desktop-first approach:

```css
.container {
  display: flex;
}

@media (max-width: 768px) {
  .container {
    display: block;
  }
}
```

Better mobile-first approach:

```css
.container {
  display: block;
}

@media (min-width: 768px) {
  .container {
    display: flex;
  }
}
```

## Why Mobile-First Is Better

- Most users browse on mobile
- Cleaner CSS
- Better performance
- Easier responsive design
- Professional frontend approach

## Mobile-First Interview Answer

Mobile-first design means writing the default CSS for small screens first, then using `min-width` media queries to enhance the layout for tablets and desktops. It is important because most users browse on mobile, and it makes responsive design cleaner and more scalable.
