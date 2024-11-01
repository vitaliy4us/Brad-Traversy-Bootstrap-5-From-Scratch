# Sizing, Borders & Shadows

Bootstrap has some classes for sizing, borders abd shadows. Let's look at them.

## Sizing

### Width

You can set the width of an element with the `w-` classes. The default is `w-auto`, which is the width of the content. You can also use `w-25`, `w-50`, `w-75`, and `w-100`. These are percentages.

```html
<div class="bg-success text-white p-3 w-25">Width 25%</div>
<div class="bg-success text-white p-3 w-50">Width 50%</div>
<div class="bg-success text-white p-3 w-75">Width 75%</div>
<div class="bg-success text-white p-3 w-100">Width 100%</div>
<div class="bg-success text-white p-3 w-auto">Width Auto</div>
```

### Height

You can set the height of an element with the `h-` classes. The default is `h-auto`, which is the height of the content. You can also use `h-25`, `h-50`, `h-75`, and `h-100`. These are percentages.

We need to define a hight for the parent element for this to work.

```html
<div style="height: 300px; border: 1px solid #333">
  <div class="bg-primary text-white d-inline-block h-25">Height 25%</div>
  <div class="bg-primary text-white d-inline-block h-50">Height 50%</div>
  <div class="bg-primary text-white d-inline-block h-75">Height 75%</div>
  <div class="bg-primary text-white d-inline-block h-100">Height 100%</div>
  <div class="bg-primary text-white d-inline-block h-auto">Height Auto</div>
</div>
```

## Borders

To add a border, you just add the class `border`. You can also add a border to indivudual sides with `border-top`, `border-right`, `border-bottom`, and `border-left`.

```html
<div class="p-3 mb-2 bg-light border">Regular</div>
<div class="p-3 mb-2 bg-light border-top">Border Top</div>
<div class="p-3 mb-2 bg-light border-bottom">Border Bottom</div>
<div class="p-3 mb-2 bg-light border-right">Border Right</div>
<div class="p-3 mb-2 bg-light border-left">Border Left</div>
```

### Border Color

You can use the color variations on borders as well:

```html
<div class="p-3 mb-2 bg-light border border-primary">Primary</div>
<div class="p-3 mb-2 bg-light border border-secondary">Secondary</div>
<div class="p-3 mb-2 bg-light border border-success">Success</div>
<div class="p-3 mb-2 bg-light border border-info">Info</div>
<div class="p-3 mb-2 bg-light border border-warning">Warning</div>
<div class="p-3 mb-2 bg-light border border-danger">Danger</div>
<div class="p-3 mb-2 bg-light border border-light">Light</div>
<div class="p-3 mb-2 bg-light border border-dark">Dark</div>
<div class="p-3 mb-2 bg-light border border-white">White</div>
```

### Border Radius

Classes for different border radiuses:

```html
<div class="p-3 mb-2 bg-light border rounded">Rounded</div>
<div class="p-3 mb-2 bg-light border rounded-top">Rounded Top</div>
<div class="p-3 mb-2 bg-light border rounded-bottom">Rounded Bottom</div>
<div class="p-3 mb-2 bg-light border rounded-right">Rounded Right</div>
<div class="p-3 mb-2 bg-light border rounded-left">Rounded Left</div>
<div class="p-3 mb-2 bg-light w-25 border rounded-circle">Rounded Circle</div>
<div class="p-3 mb-2 bg-light border rounded-1">Rounded 1</div>
<div class="p-3 mb-2 bg-light border rounded-2">Rounded 2</div>
<div class="p-3 mb-2 bg-light border rounded-3">Rounded 3</div>
<div class="p-3 mb-2 bg-light border rounded-4">Rounded 4</div>
<div class="p-3 mb-2 bg-light border rounded-5">Rounded 5</div>
```

## Shadows

Shadows are similar to borders. We have different sizes:

```html
<div class="shadow-none p-3 mb-5 rounded">No shadow</div>
<div class="shadow-sm p-3 mb-5 rounded">Small shadow</div>
<div class="shadow p-3 mb-5 rounded">Regular shadow</div>
<div class="shadow-lg p-3 mb-5 rounded">Larger shadow</div>
```
