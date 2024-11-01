# Bootstrap Grid & Columns

We have looked at a bunch of components in Bootstrap, but we haven't looked at how to lay them out. In this lesson, we will look at the Bootstrap grid and columns. This is not to be confused with `CSS Grid`. Actually, under the hood, the Bootstrap grid uses `flexbox`. There are also classes to use flexbox directly and there is actually a `grid` class that allows you to use CSS Grid, but it is still experimental and not loaded by default. You have to enable it and compile Bootstrap with Sass.

The Bootstrap grid is responsive, so there are classes for different screen sizes and breakpoints.

## Basic Grid

Let's look at a basic grid layout. You can completely ignore the `bg-light` and `border` classes. They are just there to make the grid visible. If you want a background color, you would usually add it to the content inside of the column rather than the column itself.

```html
<div class="row">
  <div class="col bg-light border">1 of 2</div>
  <div class="col bg-light border">2 of 2</div>
</div>
<div class="row">
  <div class="col bg-light border">1 of 3</div>
  <div class="col bg-light border">2 of 3</div>
  <div class="col bg-light border">3 of 3</div>
</div>
```

As you can see, there are 2 classes we use to create a grid. We have the `row` class, which is used to create a row. Then we have the `col` class, which is used to create a column. You can specify a number with the column class, but here we just used the `col` class without a number. This will make the column take up the entire width of the row.

So we have 1 row with 2 columns and another with 3. If we do not add any size or number to the column classes, they will always take up the same amount of space, even on smaller screens. So they do not stack in this case.

## Column Sizes

We can specify the size of the columns by adding a number to the column class. It is a 12 column system, so if we add the number 6 to the column class, it will take up half of the row. Let's create a row with 2 equal columns and another with 3 equal columns:

```html
<div class="row">
  <div class="col-6 bg-light border">1 of 2</div>
  <div class="col-6 bg-light border">2 of 2</div>
</div>
<div class="row">
  <div class="col-4 bg-light border">1 of 3</div>
  <div class="col-4 bg-light border">2 of 3</div>
  <div class="col-4 bg-light border">3 of 3</div>
</div>
```

Notice that we get the same result. That is because they are all equal columns. If we want to create a row with 2 columns where one is twice as big as the other, we can add the number 8 to the first column and 4 to the second:

```html
<div class="row">
  <div class="col-8 bg-light border">1 of 2</div>
  <div class="col-4 bg-light border">2 of 2</div>
</div>
```

## Column Breakpoints

So you see how this works, we simply add the number of spaces we want the column to take up to the column class. But what if we want the columns to be different sizes on different screen sizes? We can do that by adding the breakpoint to the column class. Let's say we want 2 columns that take up half of the screen on medium screens and up, but on small screens, we want them to take up the entire screen (stack). We can do that by adding the number 6 to the column class and the breakpoint `md`:

```html
<div class="row">
  <div class="col-md-6 bg-light border">1 of 2</div>
  <div class="col-md-6 bg-light border">2 of 2</div>
</div>
```

Make the browser smaller and you will see that the 2 grid columns will stack on top of each other.

Let's say we want to stack on small screens, 2 on medium screens and 4 on large screens.

```html
<div class="row">
  <div class="col-sm-12 col-md-6 col-lg-3 bg-light border">1 of 4</div>
  <div class="col-sm-12 col-md-6 col-lg-3 bg-light border">2 of 4</div>
  <div class="col-sm-12 col-md-6 col-lg-3 bg-light border">3 of 4</div>
  <div class="col-sm-12 col-md-6 col-lg-3 bg-light border">4 of 4</div>
</div>
```

## Row Columns

We can also set the number of columns in the row element by using the `row-cols-*` class. Let's say we want 2 columns in the row:

```html
<div class="row row-cols-2">
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
</div>
```

We didn't add the number to the coumn class, we added it to the row class. Now simply change the number to 3 and you will get 3 columns in the row.

```html
<div class="row row-cols-3">
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
</div>
```

You can also add the screen sizes to the row class. Let's say we want 1 column (stacked) to begin with, then 2 columns on medium screens and 4 columns on large screens:

```html
<div class="row row-cols-1 row-cols-md-2 row-cols-lg-4">
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
  <div class="col bg-light border">Column</div>
</div>
```

Now you have a responsive grid without adding anything but `.col` on the columns.

## Nesting Grids

You can also have a row within a row. Let's create a 3 column row and in the last column, we will have a nested 3 column row:

```html
<div class="row">
  <div class="col bg-light border p-5">Column</div>
  <div class="col bg-light border p-5">Column</div>
  <div class="col bg-light border p-5">
    <div class="row">
      <div class="col bg-light border">Column</div>
      <div class="col bg-light border">Column</div>
      <div class="col bg-light border">Column</div>
    </div>
  </div>
</div>
```

## Gutters

Gutter classes give us an easy way to add some spacing between the columns. Let's first create a 2 column layout.

```html
<div class="row">
  <div class="col-md-6">
    <div class="p-3 text-bg-dark">Content Item</div>
  </div>
  <div class="col-md-6">
    <div class="p-3 text-bg-dark">Content Item</div>
  </div>
  <div class="col-md-6">
    <div class="p-3 text-bg-dark">Content Item</div>
  </div>
  <div class="col-md-6">
    <div class="p-3 text-bg-dark">Content Item</div>
  </div>
</div>
```

Now add a class of `g-4` to the row element:

```html
<div class="row g-4">
  <div class="col-md-6">
    <div class="p-3 text-bg-dark">Content Item</div>
  </div>
  <div class="col-md-6">
    <div class="p-3 text-bg-dark">Content Item</div>
  </div>
  <div class="col-md-6">
    <div class="p-3 text-bg-dark">Content Item</div>
  </div>
  <div class="col-md-6">
    <div class="p-3 text-bg-dark">Content Item</div>
  </div>
</div>
```

As you can see it added spacing between the rows and columns. You can also add a class of `gx-*` to add spacing between the columns and `gy-*` to add spacing between the rows.

## Offsetting Columns

You can also offset columns. Add the following html:

```html
<div class="row">
  <div class="col-md-4">
    <div class="p-3 text-bg-primary">Content Item</div>
  </div>
  <div class="col-md-4 offset-md-4">
    <div class="p-3 text-bg-primary">Content Item</div>
  </div>
</div>
<div class="row">
  <div class="col-md-3 offset-md-3">
    <div class="p-3 text-bg-primary">Content Item</div>
  </div>
  <div class="col-md-3 offset-md-3">
    <div class="p-3 text-bg-primary">Content Item</div>
  </div>
</div>
<div class="row">
  <div class="col-md-6 offset-md-3">
    <div class="p-3 text-bg-primary">Content Item</div>
  </div>
</div>
```

As you can see, we can offset columns by adding the `offset-*` class to the column. The number you add to the class is the number of columns you want to offset. So if you add the number 4 to the class, it will offset the column by 4 columns.

## Ordering Columns

In some cases, you may want the columns to appear in a different order in general or in a different order on different screen sizes. You can do that by adding the `order-*` class to the column. Let's change the order on large screens:

```html
<div class="row">
  <div class="col order-lg-2">
    <div class="p-3 text-bg-dark">Item 1</div>
  </div>
  <div class="col order-lg-3">
    <div class="p-3 text-bg-dark">Item 2</div>
  </div>
  <div class="col order-lg-1">
    <div class="p-3 text-bg-dark">Item 3</div>
  </div>
</div>
```

You could also just use `order-1`, `order-2` and `order-3` to change the order on all screen sizes.
