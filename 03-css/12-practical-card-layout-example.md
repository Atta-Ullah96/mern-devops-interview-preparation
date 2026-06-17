# Practical CSS Card Layout Example

This practice file combines today's CSS topics:

```txt
Colors
Units
Box model
Margin
Padding
Border
Display
Position
Z-index
Overflow
Object-fit
```

## HTML

```html
<div class="card">
  <span class="badge">New</span>

  <img
    class="card-image"
    src="https://images.unsplash.com/photo-1516321318423-f06f85e504b3"
    alt="Laptop screen showing dashboard"
  />

  <div class="card-body">
    <h2 class="card-title">Storix File Preview</h2>
    <p class="card-description">
      Securely upload, preview, and download your files from cloud storage.
    </p>
    <a class="card-button" href="#">View File</a>
  </div>
</div>
```

## CSS

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background-color: #f3f4f6;
  color: #111827;
}

.card {
  width: 320px;
  margin: 2rem auto;
  background-color: #ffffff;
  border: 1px solid #e5e7eb;
  border-radius: 1rem;
  overflow: hidden;
  position: relative;
}

.badge {
  position: absolute;
  top: 1rem;
  right: 1rem;
  z-index: 10;
  display: inline-block;
  padding: 0.35rem 0.75rem;
  border-radius: 999px;
  background-color: rgba(37, 99, 235, 0.9);
  color: white;
  font-size: 0.875rem;
}

.card-image {
  display: block;
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.card-body {
  padding: 1.25rem;
}

.card-title {
  margin: 0 0 0.5rem;
  font-size: 1.25rem;
}

.card-description {
  margin: 0 0 1rem;
  color: #6b7280;
  line-height: 1.5;
}

.card-button {
  display: inline-block;
  padding: 0.75rem 1rem;
  border-radius: 0.5rem;
  background-color: #2563eb;
  color: white;
  text-decoration: none;
}
```

## What this example teaches

### Colors

```css
background-color: #ffffff;
color: #111827;
background-color: rgba(37, 99, 235, 0.9);
```

### Units

```css
width: 320px;
margin: 2rem auto;
padding: 1.25rem;
```

### Box model

```css
border: 1px solid #e5e7eb;
padding: 1.25rem;
margin: 2rem auto;
```

### Display

```css
.card-button {
  display: inline-block;
}
```

### Position and z-index

```css
.card {
  position: relative;
}

.badge {
  position: absolute;
  top: 1rem;
  right: 1rem;
  z-index: 10;
}
```

### Overflow

```css
.card {
  overflow: hidden;
}
```

This keeps the image inside the rounded card corners.

### Object-fit

```css
.card-image {
  object-fit: cover;
}
```

This makes the image fill the card image area without stretching.
