# List Groups & Badges

List groups are a flexible and powerful component for displaying a series of content. Modify and extend them to support just about any content within. They are often used for sidebars and navigation.

## List Groups

Let's create a simple list group with some names:

```html
<ul class="list-group">
  <li class="list-group-item">Tony Stark</li>
  <li class="list-group-item">Steve Rogers</li>
  <li class="list-group-item">Bruce Banner</li>
  <li class="list-group-item">Thor Odinson</li>
  <li class="list-group-item">Rick Jones</li>
</ul>
```

### Active & Disabled Items

We can make an item active by adding the `active` class to it and make it disabled by adding the `disabled` class to it:

```html
<ul class="list-group">
  <li class="list-group-item">Tony Stark</li>
  <li class="list-group-item">Steve Rogers</li>
  <li class="list-group-item active">Bruce Banner</li>
  <!-- Active Item -->
  <li class="list-group-item disabled">Thor Odinson</li>
  <!-- Disabled Item -->
  <li class="list-group-item">Rick Jones</li>
</ul>
```

# Links

it is common to use list groups as side navigation. To add links, just add an anchor tag as the list item:

```html
<div class="list-group">
  <a
    href="#"
    class="list-group-item list-group-item-action active"
    aria-current="true"
  >
    The current link item
  </a>
  <a href="#" class="list-group-item list-group-item-action">Tony Stark</a>
  <a href="#" class="list-group-item list-group-item-action">Steve Rogers</a>
  <a href="#" class="list-group-item list-group-item-action">Bruce Banner</a>
  <a class="list-group-item list-group-item-action disabled">Thor Odinson</a>
</div>
```

## Flush Style

You can get rid of the outside borders with the `list-group-flush` class:

```html
<ul class="list-group list-group-flush">
  <li class="list-group-item">Tony Stark</li>
  <li class="list-group-item">Steve Rogers</li>
  <li class="list-group-item">Bruce Banner</li>
  <li class="list-group-item">Thor Odinson</li>
  <li class="list-group-item">Rick Jones</li>
</ul>
```

## Numbered List

You can add numbers to the list items with the `list-group-numbered` class:

```html
<ol class="list-group list-group-numbered">
  <li class="list-group-item">Tony Stark</li>
  <li class="list-group-item">Steve Rogers</li>
  <li class="list-group-item">Bruce Banner</li>
</ol>
```

## Badges

Badges are small, simple components for displaying an indicator or count of some sort. They're commonly found in email clients like Gmail or on mobile app icons when a new notification is available.

```html
<h1>Example heading <span class="badge bg-primary">New</span></h1>
<h2>Example heading <span class="badge bg-secondary">New</span></h2>
<h3>Example heading <span class="badge bg-success">New</span></h3>
<h4>Example heading <span class="badge bg-danger">New</span></h4>
<h5>Example heading <span class="badge bg-info">New</span></h5>
<h6>Example heading <span class="badge bg-warning">New</span></h6>
```

### In Buttons

You can put badges in buttons:

```html
<button type="button" class="btn btn-primary">
  Notifications <span class="badge text-bg-dark">10</span>
</button>
```

### Positioned

We saw this in a past lesson, but you can position badges with the `position-absolute` class:

```html
<button type="button" class="btn btn-primary position-relative">
  Inbox
  <span
    class="position-absolute top-0 start-100 translate-middle badge rounded-pill bg-danger"
  >
    99+
    <span class="visually-hidden">unread messages</span>
  </span>
</button>
```

The `rounded-pill` class makes the badge pill-shaped.

### Badges in List Groups

It is also common to use badges in list groups:

```html
<ul class="list-group">
  <li class="list-group-item d-flex justify-content-between align-items-start">
    <div class="ms-2 me-auto">
      <div class="fw-bold">Electronics</div>
      Content for list item
    </div>
    <span class="badge bg-primary rounded-pill">20</span>
  </li>
  <li class="list-group-item d-flex justify-content-between align-items-start">
    <div class="ms-2 me-auto">
      <div class="fw-bold">Fashion</div>
      Content for list item
    </div>
    <span class="badge bg-primary rounded-pill">20</span>
  </li>
  <li class="list-group-item d-flex justify-content-between align-items-start">
    <div class="ms-2 me-auto">
      <div class="fw-bold">Sports</div>
      Content for list item
    </div>
    <span class="badge bg-primary rounded-pill">20</span>
  </li>
</ul>
```
