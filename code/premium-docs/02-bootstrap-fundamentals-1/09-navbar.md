# Navbar

Navbars are very important as it contains your website's navigation. It is usually placed at the top of the page, but for the this tutorial, we will be creating a few different types.

## Simple Navbar

Let's create a very simple navbar with a couple links.

```html
<nav class="navbar navbar-expand-lg bg-light">
  <div class="container">
    <a class="navbar-brand" href="#">Navbar</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Services</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

### A Word on Containers

Usually you will not put the navbar in a container. If you do that, the navbar will be constrained to the width of the container. This is not what you want. You want the navbar to be the full width of the screen. Usually what you want to do is put the container inside of the navbar. This will center the content of the navbar. If you want the content of the navbar to go all the way over to the right/left, you could use `container-fluid` or just not use a container.

There are a few sub components to a navbar:

- `.navbar-brand` for your company, product, or project name.
- `.navbar-nav` for a full-height and lightweight navigation (including support for dropdowns).
- `.navbar-toggler` for use with our collapse plugin and other navigation toggling behaviors.
- Flex and spacing utilities for any form controls and actions.
- `.navbar-text` for adding vertically centered strings of text.
- `.collapse.navbar-collapse` for grouping and hiding navbar contents by a parent breakpoint.
  Add an optional `.navbar-scroll` to set a max-height and scroll expanded navbar content.

The `navbar-expand` classes determine when the navbar should expand and take up the whole screen. As long as you include the JavaScript, it will have a working hamburger menu. The `navbar-expand-lg` class will expand the navbar when the screen is at least `992px` wide. Go ahead and experiment with the other breakpoints like `navbar-expand-sm`, `navbar-expand-md`, and `navbar-expand-xl`.

## Aligning Items To The Right

Just add a class of `ms-auto` to the `ul.navbar-nav` element.

```html
<nav class="navbar navbar-expand-lg bg-light">
  <div class="container">
    <a class="navbar-brand" href="#">Navbar</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <!-- ms-auto added -->
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Services</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

## Colors

You can use the color variant `bg-*` classes. Let's use the `bg-primary` class. This will not change the text. You could add `text-white`, but that will not affect the links. What you can do is add a class of `navbar-dark` to the `nav` element. This will change the text to white.

```html
<nav class="navbar navbar-expand-lg bg-primary navbar-dark">
  <div class="container">
    <a class="navbar-brand" href="#">Navbar</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Services</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

## Fixed Top

It is very common these days to stick the navbar to the top. Many websites are a single page where the navbar takes you to different sections of the page. Of course, you want users to be able to see the navbar at all times. To do this, add the class `fixed-top` to the `nav` element.

```html
<nav class="navbar navbar-expand-lg bg-dark navbar-dark fixed-top">
  <div class="container">
    <a class="navbar-brand" href="#">Navbar</a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Services</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

You can add a bunch of dummy text to test it out. You can also use the class `sticky-top` instead of `fixed-top`. The difference is that `sticky-top` will stick to the top of the screen until you scroll past it. `fixed-top` will always be at the top of the screen. If you wanted the navbar at the bottom for some reason, you can use `fixed-bottom`.

## Navbar With Form

You can also add forms in navbars. Here is a simple example:

```html
<nav class="navbar bg-dark navbar-dark">
  <div class="container-fluid">
    <a class="navbar-brand">Navbar</a>
    <form class="d-flex" role="search">
      <input
        class="form-control me-2"
        type="search"
        placeholder="Search"
        aria-label="Search"
      />
      <button class="btn btn-outline-success" type="submit">Search</button>
    </form>
  </div>
</nav>
```

## Scrolling

We used to have to do some extra JavaScript work to create a smooth scrolling effect when clicking on a link with an ID. Now it just works. Let's create a simple example.

Add an id at the bottom of the page:

```html
<div id="about"></div>
```

Then add a link to the navbar:

```html
<a class="nav-link" href="#about">Bottom</a>
```

Click on it and you should get a smooth scrolling effect.
