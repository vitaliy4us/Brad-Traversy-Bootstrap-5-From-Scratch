# Spinners

Spinners are animated loading images that are used to display while a page is loading. If you are creating very simple websites and just using Bootstrap for the CSS classes, you probably won't need to use these, but if you are creating a web app, they can be helpful and improve the UI/UX.

## Border Spinner

A border spinner is a lightweight loading indicator. Let's create one:

```html
<div class="spinner-border" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
```

## Color Spinners

you can use different classes for different colors:

```html
<div class="spinner-border text-primary" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
<div class="spinner-border text-secondary" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
<div class="spinner-border text-success" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
<div class="spinner-border text-danger" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
<div class="spinner-border text-warning" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
<div class="spinner-border text-info" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
<div class="spinner-border text-light" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
<div class="spinner-border text-dark" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
```

## Growing Spinners

You can also use a growing spinner:

```html
<div class="spinner-grow" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
```

You can use the same color classes as the border spinner.

## Alignment

Usually you want to align these in the center of the page. You can do that by wrapping them in a div with the class of `d-flex` and `justify-content-center`:

```html
<div class="d-flex justify-content-center">
  <div class="spinner-border" role="status">
    <span class="visually-hidden">Loading...</span>
  </div>
</div>
```

## Sizing

There is an `-sm` class to make them smaller:

```html
<div class="spinner-border spinner-border-sm" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
<div class="spinner-grow spinner-grow-sm" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
```

If you want them to be bigger, just add a width and height:

```html
<div class="spinner-border" style="width: 5rem; height: 5rem" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
```

## In Buttons

You can also place spinners inside of buttons:

```html
<button class="btn btn-primary" type="button" disabled>
  <span
    class="spinner-border spinner-border-sm"
    role="status"
    aria-hidden="true"
  ></span>
  Loading...
</button>
```
