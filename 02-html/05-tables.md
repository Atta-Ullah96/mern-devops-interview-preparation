# HTML Tables

## What is a Table?

A table is used to show data in rows and columns.

Tables should be used for tabular data, not for page layout.

Example use cases:

- User list
- Pricing comparison
- Order history
- Invoice items
- Reports

---

## Basic Table

```html
<table>
  <tr>
    <th>Name</th>
    <th>Role</th>
  </tr>
  <tr>
    <td>Ali</td>
    <td>Developer</td>
  </tr>
</table>
```

---

## Table Tags

### `<table>`

Creates the table.

### `<tr>`

Creates a table row.

### `<th>`

Creates a table heading cell.

### `<td>`

Creates a normal table data cell.

---

## Better Table Structure

```html
<table>
  <caption>Users List</caption>

  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Email</th>
      <th scope="col">Role</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Ali</td>
      <td>ali@example.com</td>
      <td>Admin</td>
    </tr>
    <tr>
      <td>Sara</td>
      <td>sara@example.com</td>
      <td>User</td>
    </tr>
  </tbody>
</table>
```

---

## Why use `<thead>` and `<tbody>`?

They make the table more organized and easier for browsers, screen readers, and developers to understand.

---

## What is `<caption>`?

`<caption>` gives a title or description to the table.

```html
<caption>Monthly Sales Report</caption>
```

---

## What is `scope`?

The `scope` attribute helps screen readers understand whether a header applies to a row or column.

```html
<th scope="col">Email</th>
```

---

## Interview Answer

HTML tables are used to display tabular data in rows and columns. A table uses tags like `<table>`, `<tr>`, `<th>`, and `<td>`. For better structure and accessibility, we should use `<thead>`, `<tbody>`, `<caption>`, and the `scope` attribute. Tables should be used for data, not for designing page layouts.

---

## Common Interview Questions

1. What is the purpose of an HTML table?
2. What is the difference between `<th>` and `<td>`?
3. Why should we use `<thead>` and `<tbody>`?
4. What is the purpose of `<caption>`?
5. Why should tables not be used for page layout?

---

## What I Learned

- Tables are for tabular data.
- `<th>` is for headings and `<td>` is for data cells.
- `<caption>` improves table meaning.
- `scope` improves accessibility.
- Tables should not be used for layout design.
