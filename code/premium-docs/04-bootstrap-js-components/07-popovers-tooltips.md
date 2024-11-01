# Popovers & Toolips

Popovers and tooltips are used to show additional information. These are both base on the Popper.js library. You need to make sure that you either include the Popper.js library or the `bootstrap.bundle.js` file, which includes Popper.

## Popovers

A popover is a small overlay that appears when you click on an element. Let's create one:

```html
<button
  id="popover"
  type="button"
  class="btn btn-lg btn-danger"
  data-bs-toggle="popover"
  data-bs-title="Popover title"
  data-bs-content="This is the popover content"
>
  Click to toggle popover
</button>
```

So here we have a button that will display a popover when clicked. The `data-bs-toggle` attribute tells Bootstrap that this element should toggle a popover. The `data-bs-title` attribute is the title of the popover, and the `data-bs-content` attribute is the content of the popover.

This will not work yet because we actually have to enable popovers in our JavaScript:

```js
const popoverEl = document.getElementById('popover');
const popover = new bootstrap.Popover(popoverEl);
```

You can change the side the popover appears on by adding the `data-bs-placement` attribute:

```html
<button
  id="popover"
  type="button"
  class="btn btn-lg btn-danger"
  data-bs-toggle="popover"
  data-bs-title="Popover title"
  data-bs-content="This is the popover content"
  data-bs-placement="bottom"
>
  Click to toggle popover
</button>
```

The values are `top`, `bottom`, `left`, and `right`.

## Tooltips

Tooltips are similar to popovers, but they are smaller and appear when you hover over an element. Let's create some links with some tooltips:

```html
<p class="muted">
  Here are some
  <a href="#" data-bs-toggle="tooltip" data-bs-title="Default tooltip"
    >inline links</a
  >
  with tooltips. Here is
  <a href="#" data-bs-toggle="tooltip" data-bs-title="Another tooltip"
    >another link </a
  >.
</p>
```

This will not work yet because we actually have to enable tooltips in our JavaScript:

```js
const tooltipTriggerList = document.querySelectorAll(
  '[data-bs-toggle="tooltip"]'
);
const tooltipList = [...tooltipTriggerList].map(
  (tooltipTriggerEl) => new bootstrap.Tooltip(tooltipTriggerEl)
);
```

This time, we selected the elements with the `data-bs-toggle="tooltip"` attribute and created a tooltip for each one.
