# Spacing

Margin and padding are very important. We use them all the time. Bootstrap has a lot of utility classes for spacing. Let's look at some of them. I will be using some background color classes to make the spacing more visible.

## Margin

Margin is of course the space outside of an element. There are classes for margin on all sides, top, bottom, left, and right.

### Margin on All Sides

These classes will add margin on every side of an element.

```html
<div class="bg-dark m-1">Lorem, ipsum dolor.</div>
<div class="bg-dark text-white">Lorem, ipsum dolor.</div>
<div class="bg-dark text-white">Lorem, ipsum dolor.</div>
<div class="bg-dark text-white">Lorem, ipsum dolor.</div>
<div class="bg-dark text-white">Lorem, ipsum dolor.</div>
```

As you can see, the top div has margin all around it. The other divs have no margin.

The default variations of 1-5 are as follows:

- 1: 0.25rem
- 2: 0.5rem
- 3: 1rem
- 4: 1.5rem
- 5: 3rem

Remember, the default font-size is 16px, so 1rem is 16px. 0.25rem is 4px, 0.5rem is 8px, 1.5rem is 24px, and 3rem is 48px.

Let's use some of the other variations.

```html
<div class="bg-dark m-1">Lorem, ipsum dolor.</div>
<div class="bg-dark m-2">Lorem, ipsum dolor.</div>
<div class="bg-dark m-3">Lorem, ipsum dolor.</div>
<div class="bg-dark m-4">Lorem, ipsum dolor.</div>
<div class="bg-dark m-5">Lorem, ipsum dolor.</div>
```

As you can see, the margin increases with each variation.

### Top and Bottom Margin

These classes will add margin on the top and bottom of an element. This is the `Y` axis.

```html
<div class="text-bg-success my-1">Lorem, ipsum dolor.</div>
<div class="text-bg-success my-2">Lorem, ipsum dolor.</div>
<div class="text-bg-success my-3">Lorem, ipsum dolor.</div>
<div class="text-bg-success my-4">Lorem, ipsum dolor.</div>
<div class="text-bg-success my-5">Lorem, ipsum dolor.</div>
```

### Left and Right Margin

These classes will add margin on the left and right of an element. This is the `X` axis.

```html
<div class="text-bg-secondary mx-1">Lorem, ipsum dolor.</div>
<div class="text-bg-secondary mx-2">Lorem, ipsum dolor.</div>
<div class="text-bg-secondary mx-3">Lorem, ipsum dolor.</div>
<div class="text-bg-secondary mx-4">Lorem, ipsum dolor.</div>
<div class="text-bg-secondary mx-5">Lorem, ipsum dolor.</div>
```

### Top Margin

We can use the `mt` class to add margin on the top of an element.

```html
<div class="text-bg-danger mt-1">Lorem, ipsum dolor.</div>
<div class="text-bg-danger mt-2">Lorem, ipsum dolor.</div>
<div class="text-bg-danger mt-3">Lorem, ipsum dolor.</div>
<div class="text-bg-danger mt-4">Lorem, ipsum dolor.</div>
<div class="text-bg-danger mt-5">Lorem, ipsum dolor.</div>
```

### Bottom Margin

We can use the `mb` class to add margin on the bottom of an element.

```html
<div class="text-bg-warning mb-1">Lorem, ipsum dolor.</div>
<div class="text-bg-warning mb-2">Lorem, ipsum dolor.</div>
<div class="text-bg-warning mb-3">Lorem, ipsum dolor.</div>
<div class="text-bg-warning mb-4">Lorem, ipsum dolor.</div>
<div class="text-bg-warning mb-5">Lorem, ipsum dolor.</div>
```

### Margin Left/Start

We can use the `ms` class to add margin on the left or the start of an element.

```html
<div class="text-bg-info ms-1">Lorem, ipsum dolor.</div>
<div class="text-bg-info ms-2">Lorem, ipsum dolor.</div>
<div class="text-bg-info ms-3">Lorem, ipsum dolor.</div>
<div class="text-bg-info ms-4">Lorem, ipsum dolor.</div>
<div class="text-bg-info ms-5">Lorem, ipsum dolor.</div>
```

### Margin Right/End

We can use the `me` class to add margin on the right or the end of an element.

```html
<div class="text-bg-dark me-1">Lorem, ipsum dolor.</div>
<div class="text-bg-dark me-2">Lorem, ipsum dolor.</div>
<div class="text-bg-dark me-3">Lorem, ipsum dolor.</div>
<div class="text-bg-dark me-4">Lorem, ipsum dolor.</div>
<div class="text-bg-dark me-5">Lorem, ipsum dolor.</div>
```

### Margin Auto

There are also classes for margin `auto`. Auto means that the browser will automatically calculate the margin. This is useful for centering elements.

To give you an example of this, I will also use the `w-50` class, which means width 50%. This will make the divs half the width of the screen.

```html
<div class="text-bg-warning m-auto w-50">Lorem, ipsum dolor.</div>
<div class="text-bg-warning my-auto w-50">Lorem, ipsum dolor.</div>
<div class="text-bg-warning mx-auto w-50">Lorem, ipsum dolor.</div>
<div class="text-bg-warning ms-auto w-50">Lorem, ipsum dolor.</div>
<div class="text-bg-warning me-auto w-50">Lorem, ipsum dolor.</div>
```

## Padding

Padding is the spacing inside of an element. There are classes for padding on all sides, top, bottom, left, and right.

I will use a different background color for the padding examples as well as the `.my-2` class to space them out a bit.

### Padding on All Sides

```html
<div class="text-bg-dark my-2 p-1">Lorem, ipsum dolor.</div>
<div class="text-bg-dark my-2 p-2">Lorem, ipsum dolor.</div>
<div class="text-bg-dark my-2 p-3">Lorem, ipsum dolor.</div>
<div class="text-bg-dark my-2 p-4">Lorem, ipsum dolor.</div>
<div class="text-bg-dark my-2 p-5">Lorem, ipsum dolor.</div>
```

### Top and Bottom Padding

```html
<div class="text-bg-success my-2 py-1">Lorem, ipsum dolor.</div>
<div class="text-bg-success my-2 py-2">Lorem, ipsum dolor.</div>
<div class="text-bg-success my-2 py-3">Lorem, ipsum dolor.</div>
<div class="text-bg-success my-2 py-4">Lorem, ipsum dolor.</div>
<div class="text-bg-success my-2 py-5">Lorem, ipsum dolor.</div>
```

### Left and Right Padding

```html
<div class="text-bg-danger my-2 px-1">Lorem, ipsum dolor.</div>
<div class="text-bg-danger my-2 px-2">Lorem, ipsum dolor.</div>
<div class="text-bg-danger my-2 px-3">Lorem, ipsum dolor.</div>
<div class="text-bg-danger my-2 px-4">Lorem, ipsum dolor.</div>
<div class="text-bg-danger my-2 px-5">Lorem, ipsum dolor.</div>
```

### Top Padding

```html
<div class="bg-primary my-2 pt-1">Lorem, ipsum dolor.</div>
<div class="bg-primary my-2 pt-2">Lorem, ipsum dolor.</div>
<div class="bg-primary my-2 pt-3">Lorem, ipsum dolor.</div>
<div class="bg-primary my-2 pt-4">Lorem, ipsum dolor.</div>
<div class="bg-primary my-2 pt-5">Lorem, ipsum dolor.</div>
```

### Bottom Padding

```html
<div class="text-bg-info my-2 pb-1">Lorem, ipsum dolor.</div>
<div class="text-bg-info my-2 pb-2">Lorem, ipsum dolor.</div>
<div class="text-bg-info my-2 pb-3">Lorem, ipsum dolor.</div>
<div class="text-bg-info my-2 pb-4">Lorem, ipsum dolor.</div>
<div class="text-bg-info my-2 pb-5">Lorem, ipsum dolor.</div>
```

### Left Padding

```html
<div class="text-bg-warning my-2 ps-1">Lorem, ipsum dolor.</div>
<div class="text-bg-warning my-2 ps-2">Lorem, ipsum dolor.</div>
<div class="text-bg-warning my-2 ps-3">Lorem, ipsum dolor.</div>
<div class="text-bg-warning my-2 ps-4">Lorem, ipsum dolor.</div>
<div class="text-bg-warning my-2 ps-5">Lorem, ipsum dolor.</div>
```

### Right Padding

```html
<div class="text-bg-primary my-2 pe-1">Lorem, ipsum dolor.</div>
<div class="text-bg-primary my-2 pe-2">Lorem, ipsum dolor.</div>
<div class="text-bg-primary my-2 pe-3">Lorem, ipsum dolor.</div>
<div class="text-bg-primary my-2 pe-4">Lorem, ipsum dolor.</div>
<div class="text-bg-primary my-2 pe-5">Lorem, ipsum dolor.</div>
```



## Stacks

If you have a bunch of items that you want to add equal margin to, you can use the `stack` class.

Here is an example of a vertical stack:

```html
<div class="vstack gap-3">
  <div class="p-2 bg-info">First item</div>
  <div class="p-2 bg-info">Second item</div>
  <div class="p-2 bg-info">Third item</div>
</div>
```

Here is an example of a horizontal stack:

```html
<div class="hstack gap-3">
  <div class="p-2 text-bg-success">First item</div>
  <div class="p-2 text-bg-success">Second item</div>
  <div class="p-2 text-bg-success">Third item</div>
</div>
```
