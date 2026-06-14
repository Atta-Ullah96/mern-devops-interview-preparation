# Forms, Inputs, Labels, and Buttons

## What is a Form?

A form is used to collect user input.

Examples:

- Login form
- Signup form
- Contact form
- Checkout form
- File upload form
- Search form

---

## Basic Form

```html
<form action="/login" method="POST">
  <label for="email">Email</label>
  <input id="email" name="email" type="email" required />

  <label for="password">Password</label>
  <input id="password" name="password" type="password" required />

  <button type="submit">Login</button>
</form>
```

---

## Important Form Attributes

### `action`

The URL where form data is sent.

```html
<form action="/login">
```

### `method`

The HTTP method used to submit data.

```html
<form method="POST">
```

Common methods:

- `GET`: sends data in URL query string.
- `POST`: sends data in request body.

---

## What is an Input?

An input collects data from users.

```html
<input type="text" />
```

Common input types:

```html
<input type="text" />
<input type="email" />
<input type="password" />
<input type="number" />
<input type="checkbox" />
<input type="radio" />
<input type="file" />
<input type="date" />
```

---

## What is a Label?

A label describes an input.

```html
<label for="email">Email</label>
<input id="email" type="email" />
```

The `for` attribute should match the input `id`.

Labels are important because:

- They improve accessibility.
- They help screen readers.
- Clicking the label focuses the related input.

---

## What is the `name` Attribute?

The `name` attribute identifies the field when form data is submitted.

```html
<input name="email" type="email" />
```

Without `name`, the field may not be included in form submission.

---

## Buttons

### Submit Button

```html
<button type="submit">Submit</button>
```

### Normal Button

```html
<button type="button">Open Modal</button>
```

### Reset Button

```html
<button type="reset">Reset</button>
```

Important: Inside a form, the default button type is usually submit, so use `type="button"` when the button should not submit the form.

---

## Textarea

Used for multi-line text.

```html
<label for="message">Message</label>
<textarea id="message" name="message"></textarea>
```

---

## Select Dropdown

```html
<label for="role">Role</label>
<select id="role" name="role">
  <option value="user">User</option>
  <option value="admin">Admin</option>
</select>
```

---

## File Upload Input

```html
<label for="file">Upload File</label>
<input id="file" name="file" type="file" />
```

For file upload forms using traditional submission, we often use:

```html
<form enctype="multipart/form-data">
```

---

## Real MERN Example

In a React or Next.js app, we usually handle form submission with JavaScript.

Example flow:

1. User fills login form.
2. Frontend captures email and password.
3. Frontend sends HTTP request to Express backend.
4. Backend validates user.
5. Backend sends response.

---

## Interview Answer

HTML forms are used to collect user input. A form can contain inputs, labels, textareas, selects, and buttons. Labels are important for accessibility because they connect text with form controls. Inputs collect different types of data using types like text, email, password, number, file, and checkbox. The form can submit data using methods like GET or POST.

---

## Common Interview Questions

1. What is the purpose of a form?
2. What is the difference between GET and POST in forms?
3. Why is the `label` tag important?
4. Why do inputs need a `name` attribute?
5. What is the difference between `type="submit"` and `type="button"`?

---

## What I Learned

- Forms collect user input.
- Inputs have different types.
- Labels improve accessibility.
- Buttons should have correct types.
- File uploads use file inputs and sometimes multipart form data.
