# Buttons

Bootstrap has all kinds of button classes for different styles, colors, sizes, and states. Let's take a look at some of them.

## Button Styles

Bootstrap has a few different button styles that you can use. These are the classes along with the default colors for each one:

- `btn-primary` - blue
- `btn-secondary` - gray
- `btn-success` - green
- `btn-danger` - red
- `btn-warning` - yellow
- `btn-info` - light blue
- `btn-light` - light gray
- `btn-dark` - dark gray
- `btn-link` - no color

You must also use the class `btn` with these classes. Let's try it out.

In your HTML file, add the following code:

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Danger</button>
<button class="btn btn-warning">Warning</button>
<button class="btn btn-info">Info</button>
<button class="btn btn-light">Light</button>
<button class="btn btn-dark">Dark</button>
<button class="btn btn-link">Link</button>
```

## Button Sizes

You can also change the size of the buttons. The sizes are:

- `btn-sm` - small
- `btn-lg` - large

Let's try it out.

In your HTML file, add the following code:

```html
<button class="btn btn-primary">Regular</button>
<button class="btn btn-secondary btn-sm">Small</button>
<button class="btn btn-success btn-lg">Large</button>
```

## Button States

You can also change the state of the buttons. The states are:

- `disabled` - disables the button
- `active` - makes the button look pressed

Let's try it out.

In your HTML file, add the following code:

```html
<button class="btn btn-primary">Regular</button>
<button class="btn btn-primary disabled">Disabled</button>
<button class="btn btn-primary active">Active</button>
```

## Outline Buttons

You can also make buttons that are outlined instead of filled in. To do this, add the class `btn-outline-primary` (or whatever color you want) to the button. Let's try it out.

In your HTML file, add the following code:

```html
<button class="btn btn-outline-primary">Primary</button>
<button class="btn btn-outline-secondary">Secondary</button>
<button class="btn btn-outline-success">Success</button>
<button class="btn btn-outline-danger">Danger</button>
<button class="btn btn-outline-warning">Warning</button>
<button class="btn btn-outline-info">Info</button>
<button class="btn btn-outline-light">Light</button>
<button class="btn btn-outline-dark">Dark</button>
```

## Link Buttons

We can also use the button classes on links. Let's try it out.

In your HTML file, add the following code:

```html
<a href="#" class="btn btn-primary">Link Button</a>
<a href="#" class="btn btn-secondary">Link Button</a>
<a href="#" class="btn btn-success">Link Button</a>
```

## Block Buttons

A block button stretches accross it's container. We used to use the `btn-block` class for this, but now we use the `d-grid` class. Let's try it out.

```html
<div class="d-grid gap-2">
  <button class="btn btn-primary" type="button">Button</button>
  <button class="btn btn-primary" type="button">Button</button>
</div>
```

We will learn more about grid classes later.

## Button Groups

We can group buttons together with the `btn-group` class.

```html
<div class="btn-group" role="group" aria-label="Basic example">
  <button type="button" class="btn btn-primary">Left</button>
  <button type="button" class="btn btn-primary">Middle</button>
  <button type="button" class="btn btn-primary">Right</button>
</div>
```

## Button Toolbars

We can also group button groups together with the `btn-toolbar` class.

```html
<div class="btn-toolbar" role="toolbar" aria-label="Toolbar with button groups">
  <div class="btn-group me-2" role="group" aria-label="First group">
    <button type="button" class="btn btn-primary">1</button>
    <button type="button" class="btn btn-primary">2</button>
    <button type="button" class="btn btn-primary">3</button>
    <button type="button" class="btn btn-primary">4</button>
  </div>
  <div class="btn-group me-2" role="group" aria-label="Second group">
    <button type="button" class="btn btn-secondary">5</button>
    <button type="button" class="btn btn-secondary">6</button>
    <button type="button" class="btn btn-secondary">7</button>
  </div>
  <div class="btn-group" role="group" aria-label="Third group">
    <button type="button" class="btn btn-info">8</button>
  </div>
</div>
```

## Dropdown Button

We can create dropdowns as long as you included the Bootstrap JavaScript file. Let's try it out.

```html
<div class="dropdown">
  <button
    class="btn btn-secondary dropdown-toggle"
    type="button"
    data-bs-toggle="dropdown"
    aria-expanded="false"
  >
    Dropdown button
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">Action</a></li>
    <li><a class="dropdown-item" href="#">Another action</a></li>
    <li><a class="dropdown-item" href="#">Something else here</a></li>
  </ul>
</div>
```
