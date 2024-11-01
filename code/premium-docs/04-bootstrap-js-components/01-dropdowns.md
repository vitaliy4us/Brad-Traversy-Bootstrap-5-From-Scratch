# Dropdowns

Dropdowns are toggleable, contextual overlays for displaying lists of links and more. They’re made interactive with the included Bootstrap dropdown JavaScript plugin. You need to include the JavaScript bundle in order for them to work.

## Single Button Dropdowns

To include a dropdown with a button, just use the class of `dropdown-toggle` on the button and then use the class of `dropdown-menu` on a `<ul>` element. You can then add `<li>` elements with `<a>` elements inside of them.

```html
<div class="dropdown">
  <button
    class="btn btn-primary dropdown-toggle"
    type="button"
    data-bs-toggle="dropdown"
    aria-expanded="false"
  >
    Dropdown
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">Item 1</a></li>
    <li><a class="dropdown-item" href="#">Item 2</a></li>
    <li><a class="dropdown-item" href="#">Item 3</a></li>
  </ul>
</div>
```

You can do the same with a link. You can also use any color variation classes.

## Split Button

You can also create a button that is split where only the right side triggers the dropdown. You can also create seperators in the dropdown menu.

```html
<div class="btn-group">
  <button type="button" class="btn btn-danger">Action</button>
  <button
    type="button"
    class="btn btn-danger dropdown-toggle dropdown-toggle-split"
    data-bs-toggle="dropdown"
    aria-expanded="false"
  >
    <span class="visually-hidden">Toggle Dropdown</span>
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">Item 1</a></li>
    <li><a class="dropdown-item" href="#">Item 2</a></li>
    <li><a class="dropdown-item" href="#">Item 3</a></li>
    <li><hr class="dropdown-divider" /></li>
    <li><a class="dropdown-item" href="#">Item 4</a></li>
  </ul>
</div>
```

## Dark Dropdowns

You can make the dropdown dark by adding the class of `dropdown-menu-dark` to the `<ul>` element.

```html
<div class="dropdown">
  <button
    class="btn btn-dark dropdown-toggle"
    type="button"
    data-bs-toggle="dropdown"
    aria-expanded="false"
  >
    Dropdown
  </button>
  <ul class="dropdown-menu dropdown-menu-dark">
    <li><a class="dropdown-item" href="#">Item 1</a></li>
    <li><a class="dropdown-item" href="#">Item 2</a></li>
    <li><a class="dropdown-item" href="#">Item 3</a></li>
  </ul>
</div>
```

## Dropup

You can also make the menu open from the top by using the class of `dropup` on the `<div>` element.

```html
<div class="btn-group dropup">
  <button
    type="button"
    class="btn btn-secondary dropdown-toggle"
    data-bs-toggle="dropdown"
    aria-expanded="false"
  >
    Dropup
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">Item 1</a></li>
    <li><a class="dropdown-item" href="#">Item 2</a></li>
    <li><a class="dropdown-item" href="#">Item 3</a></li>
  </ul>
</div>
```

## Navbar With Dropdowns

You can easily put a dropdown in your navigation:

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container">
    <a class="navbar-brand" href="#">Navbar</a>
    <div class="collapse navbar-collapse">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item dropdown">
          <a
            class="nav-link dropdown-toggle"
            href="#"
            role="button"
            data-bs-toggle="dropdown"
            aria-expanded="false"
          >
            Dropdown
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Item 1</a></li>
            <li><a class="dropdown-item" href="#">Item 2</a></li>
            <li><a class="dropdown-item" href="#">Item 3</a></li>
          </ul>
        </li>
      </ul>
    </div>
  </div>
</nav>
```
