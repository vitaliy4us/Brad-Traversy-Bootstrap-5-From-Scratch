# Alerts and Progress Bars

Now we are going to look at some classes to add alerts with different colors/states as well as progress bars.

## Alerts

Let's start with alerts. We can add an alert with the `alert` class and then add a class for the color:

```html
<div class="alert alert-primary" role="alert">This is a primary alert!</div>
<div class="alert alert-secondary" role="alert">This is a secondary alert!</div>
<div class="alert alert-success" role="alert">This is a success alert!</div>
<div class="alert alert-danger" role="alert">This is a danger alert!</div>
<div class="alert alert-warning" role="alert">This is a warning alert!</div>
<div class="alert alert-info" role="alert">This is a info alert!</div>
<div class="alert alert-light" role="alert">This is a light alert!</div>
<div class="alert alert-dark" role="alert">This is a dark alert!</div>
```

We use the `role` attribute to tell screen readers what the purpose of the element is. In this case, it is an alert.

### Alert Links

You can use the class of `alert-link` to make links the correct color for the alert

```html
<div class="alert alert-primary" role="alert">
  This is a primary alert with
  <a href="#" class="alert-link">an example link</a>
</div>
```

### Additional Content

You can add additional content to the alert by adding it inside of the alert div:

```html
<div class="alert alert-success" role="alert">
  <h4 class="alert-heading">Well done!</h4>
  <p>
    Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem consectetur
    deleniti totam assumenda exercitationem aspernatur, cumque nostrum iusto at
    eos.
  </p>
  <hr />
  <p class="mb-0">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus,
    dolorem.
  </p>
</div>
```

### Dismissing Alerts

You can also include a button to dismiss:

```html
<div class="alert alert-warning alert-dismissible fade show" role="alert">
  This is a dismissable alert
  <button
    type="button"
    class="btn-close"
    data-bs-dismiss="alert"
    aria-label="Close"
  ></button>
</div>
```

## Progress Bars

Progress bars are used to show the progress of a task. Use the `progress` class to create a progress bar container and use the class`progress-bar` for the filled up part. We can also set the widths by using the css `width` property and set the background color on the same div as the `progress-bar` class. i am also going to add a margin bottom to each of these so that they are spaced out a little bit.

Here are some examples:

```html
<div
  class="progress mb-4"
  role="progressbar"
  aria-label="Basic example"
  aria-valuenow="0"
  aria-valuemin="0"
  aria-valuemax="100"
>
  <div class="progress-bar" style="width: 0%"></div>
</div>
<div
  class="progress mb-4"
  role="progressbar"
  aria-label="Basic example"
  aria-valuenow="25"
  aria-valuemin="0"
  aria-valuemax="100"
>
  <div class="progress-bar" style="width: 25%"></div>
</div>
<div
  class="progress mb-4"
  role="progressbar"
  aria-label="Basic example"
  aria-valuenow="50"
  aria-valuemin="0"
  aria-valuemax="100"
>
  <div class="progress-bar bg-success " style="width: 50%"></div>
</div>
<div
  class="progress mb-4"
  role="progressbar"
  aria-label="Basic example"
  aria-valuenow="75"
  aria-valuemin="0"
  aria-valuemax="100"
>
  <div class="progress-bar bg-danger" style="width: 75%"></div>
</div>
<div
  class="progress mb-4"
  role="progressbar"
  aria-label="Basic example"
  aria-valuenow="100"
  aria-valuemin="0"
  aria-valuemax="100"
>
  <div class="progress-bar bg-info" style="width: 100%"></div>
</div>
```

As you can see, it is filled up to the percentage that we set in the `style` attribute.

### Labels

We can add a label inside of the progress bar to show the percentage:

```html
<div
  class="progress"
  role="progressbar"
  aria-label="Example with label"
  aria-valuenow="25"
  aria-valuemin="0"
  aria-valuemax="100"
>
  <div class="progress-bar" style="width: 25%">25%</div>
</div>
```

### Stripes

You can have striped progress bars by adding the class of `progress-bar-striped`:

```html
<div
  class="progress mb-4"
  role="progressbar"
  aria-label="Default striped example"
  aria-valuenow="10"
  aria-valuemin="0"
  aria-valuemax="100"
>
  <div class="progress-bar progress-bar-striped" style="width: 10%"></div>
</div>
```

### Animated Stripes

You can also animate the stripes by adding the class of `progress-bar-animated`:

```html
<div
  class="progress mb-4"
  role="progressbar"
  aria-label="Animated striped example"
  aria-valuenow="75"
  aria-valuemin="0"
  aria-valuemax="100"
>
  <div
    class="progress-bar progress-bar-striped progress-bar-animated bg-danger"
    style="width: 75%"
  ></div>
</div>
```
