# Other CSS Utilities

Let's look at some other class utilities that can be used to style elements.

## Text Truncation

This can come in handy. If you have a long string of text that maybe comes from a database, etc, you can use the `text-truncate` class to truncate the text.

```html
<!-- Block level -->
<div class="row">
  <div class="col-2 text-truncate">
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Eaque in tenetur a
    nam voluptatibus praesentium ab voluptatem rem. Nesciunt, quasi!
  </div>
</div>
```

The text will truncate to the point where the container ends. In this case, we have a column that is 2 columns wide, so the text will truncate to the end of the column. Change it to 3 columns and it will truncate to the end of the 3 columns.

## Stretched Link

This is a new utility class in Bootstrap 5. It will stretch the link to the full width of the parent element.

Let's create a card with an image, text and button link.

```html
<div class="card" style="width: 18rem">
  <img src="https://picsum.photos/200" class="card-img-top" alt="..." />
  <div class="card-body">
    <h5 class="card-title">Card with stretched link</h5>
    <p class="card-text">
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Recusandae,
      assumenda!
    </p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
```

Right now, you have to click the button/link to go to the link. But if we add the `stretched-link` class to the link, we can click anywhere in the card to go to the link.

```html
<a href="#" class="btn btn-primary stretched-link">Go somewhere</a>
```

## Invisible & Visible

If you want to hide an element visually, but still have it take up space on the page, you can use the `invisible` class. This will hide the element, but it will still be accessible to screen readers.

```html
<div class="visible">...</div>
<div class="invisible">...</div>
<div class="visible">...</div>
```

You can see the second div is invisible, but it still takes up space on the page.

## Floats

Floats are not used much now that we have flexbox and the grid. You can float elements to the left or right using the `float-left` or `float-right` classes.

```html
<div class="float-start">Float start on all viewport sizes</div>
<br />
<div class="float-end">Float end on all viewport sizes</div>
<br />
<div class="float-none">Don't float on all viewport sizes</div>
```

There are also responsive float classes, for example:

```html
<div class="float-lg-end">Float on large screens</div>
```

This will only float end on large screens
