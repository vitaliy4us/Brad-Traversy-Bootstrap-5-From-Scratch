# Tables

Tables are not realy something that are all that common anymore. However, there are cases where you may want to display tabular data. Bootstrap has classes to create and style tables.

## Basic Table

```html
<table class="table">
  <thead>
    <tr>
      <th>#</th>
      <th>Name</th>
      <th>Email</th>
      <th>Position</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Tony Stark</td>
      <td>ironman@gmail.com</td>
      <td>Senior Web Developer</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Steve Rogers</td>
      <td>captain@gmail.com</td>
      <td>UI Designer</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bruce Banner</td>
      <td>hulk@gmail.com</td>
      <td>Junior Web Developer</td>
    </tr>
  </tbody>
</table>
```

## Variants

We can use our color classes to style the table. The classes `table-*` can be added to the table, a row or even a single column.

```html
<table class="table table-dark">
  <thead>
    <tr>
      <th>#</th>
      <th>Name</th>
      <th>Email</th>
      <th>Position</th>
    </tr>
  </thead>
  <tbody>
    <tr class="table-danger">
      <th>1</th>
      <td>Tony Stark</td>
      <td>ironman@gmail.com</td>
      <td>Senior Web Developer</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Steve Rogers</td>
      <td class="table-info">captain@gmail.com</td>
      <td>UI Designer</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bruce Banner</td>
      <td>hulk@gmail.com</td>
      <td>Junior Web Developer</td>
    </tr>
  </tbody>
</table>
```

## Striped Tables

We can use the `table-striped` class to add zebra-striping to any table row within the `<tbody>`.

```html
<table class="table table-striped">
  <thead>
    <tr>
      <th>#</th>
      <th>Name</th>
      <th>Email</th>
      <th>Position</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Tony Stark</td>
      <td>ironman@gmail.com</td>
      <td>Senior Web Developer</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Steve Rogers</td>
      <td>captain@gmail.com</td>
      <td>UI Designer</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Bruce Banner</td>
      <td>hulk@gmail.com</td>
      <td>Junior Web Developer</td>
    </tr>
  </tbody>
</table>
```

## Hoverable Rows

We can use the `table-hover` class to enable a hover state on table rows within a `<tbody>`.

```html
<table class="table table-hover">
  <thead>
    <tr>
      <th>#</th>
      <th>Name</th>
      <th>Email</th>
      <th>Position</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Tony Stark</td>
      <td>ironman@gmail.com</td>
      <td>Senior Web Developer</td>
    </tr>
  </tbody>
</table>
```

## Boredered Table

We can use the `table-bordered` class to add borders on all sides of the table and cells.

```html
<table class="table table-hover table-bordered">
  <thead>
    <tr>
      <th>#</th>
      <th>Name</th>
      <th>Email</th>
      <th>Position</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Tony Stark</td>
      <td>ironman@gmail.com</td>
      <td>Senior Web Developer</td>
    </tr>
  </tbody>
</table>
```

## Borderless Tables

We can use the `table-borderless` class to remove borders on all sides of the table and cells.

```html
<table class="table table-hover table-borderless">
  <thead>
    <tr>
      <th>#</th>
      <th>Name</th>
      <th>Email</th>
      <th>Position</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Tony Stark</td>
      <td>ironman@gmail.com</td>
      <td>Senior Web Developer</td>
    </tr>
  </tbody>
</table>
```

There are a few more classes that you can use with tables, but I don't want to spend too much time on this because you probably won't use them very often if ever.
