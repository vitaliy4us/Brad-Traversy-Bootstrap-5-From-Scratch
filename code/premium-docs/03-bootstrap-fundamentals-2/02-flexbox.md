# Flexbox

Using the grid is the most common way to create overall layouts, however, there are also flexbox classes that are great for aligning content inside of the main layout. If you have a horizontal menu or a hero with different elements that you want to align in a row or a column, flexbox is a great option.

## Flexbox Classes

You can make any element a flexbox, by adding the class of `d-flex` to it. This will make all of the children of that element flex items. You can then use the flexbox utility classes to align the items.

```html
<div class="d-flex">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>
```

These items should now be horizontal, which is a flex row.

### Flex Direction

You can use the class `flex-row` to make sure it is a row, but that is the default. You can also use `flex-row-reverse`, which will reverse the order of the items.

You can change the direction to a vertical column with the class of `flex-column`:

```html
<div class="d-flex flex-column">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>
```

These direction classes also have the option to use a screen size. Let's say you want the flex items to be in a column on mobile, but a row on medium screens and up:

```html
<div class="d-flex flex-column flex-md-row">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>
```

### Flex Wrap

If you have a lot of flex items and you want them to wrap into the next row, you can use the class `flex-wrap`:

```html
<div class="d-flex flex-wrap">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>
```

### Justify Content

Justify content is used to align the items horizontally in a row or vertically in a column.

The options that you have are:

- `justify-content-start`
- `justify-content-end`
- `justify-content-center`
- `justify-content-between`
- `justify-content-around`

Go ahead and try some of these out:

```html
<div class="d-flex justify-content-end">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>

<div class="d-flex justify-content-around">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>

<div class="d-flex justify-content-between">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>

<div class="d-flex flex-column justify-content-around" style="height: 300px">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>
```

### Align Items

Align items is used to align the items vertically in a row or horizontally in a column.

The options that you have are:

- `align-items-start`
- `align-items-end`
- `align-items-center`
- `align-items-baseline`
- `align-items-stretch`

Go ahead and try some of these out:

```html
<div class="d-flex flex-column align-items-end" style="height: 300px">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>

<div class="d-flex flex-column align-items-center" style="height: 300px">
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>
```

### Align Self

You can align individual items using align self classes:

- `align-self-start`
- `align-self-end`
- `align-self-center`
- `align-self-baseline`
- `align-self-stretch`

```html
<div class="d-flex flex-column" style="height: 300px">
  <div class="text-bg-dark p-3 align-self-center">Flex Item</div>
  <div class="text-bg-dark p-3 align-self-end">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>
```

### Flex Grow

You can use `flex-grow` and `flex-shrink` classes to change how the items grow and shrink. By default, they will all grow and shrink equally. If you want one item to grow more than the others, you can use the `flex-grow-1` class on that item.

```html
<div class="d-flex">
  <div class="text-bg-primary p-3 flex-grow-1">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
  <div class="text-bg-dark p-3">Flex Item</div>
</div>
```
