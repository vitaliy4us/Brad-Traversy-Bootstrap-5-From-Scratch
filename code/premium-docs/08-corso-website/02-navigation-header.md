# Navigation & Header

We will start very similar to how we will start with all of these projects and that is with the navbar and the header/hero area. The navbar is pretty simple. It will have a logo, a few links that direct the user to a certain section and a few social icons.

The header/hero area will have a background image, some text and a couple buttons. It will also have a carousel widget that we will add in the next video.

## The Navbar

Open the `index.html` file and add the following code:

```html
<!-- Navigation -->
<nav class="navbar navbar-expand-lg fixed-top navbar-dark">
  <div class="container">
    <a class="navbar-brand" href="/#">
      <img src="images/logo.png" alt="" width="150" />
    </a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNavDropdown"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link" aria-current="page" href="/#home">Home</a>
        </li>

        <li class="nav-item">
          <a class="nav-link" href="/#discover">Discover</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/#summary">Summary</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/#takeaways">Takeaways</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/#subscribe">Subscribe</a>
        </li>
      </ul>
      <span class="nav-item">
        <span class="fa-stack">
          <a href="https://facebook.com" target="_blank">
            <i class="fas fa-circle fa-stack-2x"></i>
            <i class="fab fa-facebook-f fa-stack-1x text-white"></i>
          </a>
        </span>
        <span class="fa-stack">
          <a href="https://twitter.com" target="_blank">
            <i class="fas fa-circle fa-stack-2x"></i>
            <i class="fab fa-twitter fa-stack-1x text-white"></i>
          </a>
        </span>
      </span>
    </div>
  </div>
</nav>
```

Most of this is pretty standard Bootstrap markup. For the icons, we used the `fa-stack` class to stack the circle and the icon. We also used the `fa-stack-2x` and `fa-stack-1x` classes to make the circle bigger than the icon and added `text-white` class to make the icon white.

## The Header

We will add the header without the carousel first. Open the `index.html` file and add the following code:

```html
<!-- Header -->
<header class="header py-7 vh-100">
  <div class="container">
    <div class="row mb-5 text-center">
      <div class="col-12 text-container">
        <h1 class="display-2 text-white mt-3">
          Explore Our Training and Seminar Videos
        </h1>
        <p class="lead text-white w-75 m-auto mb-4">
          Whether you're a beginner or an experienced professional, our
          carefully curated content will empower you to enhance your skills and
          expand your knowledge
        </p>
        <a class="btn btn-primary text-uppercase" href="#register">Register</a>
        <a class="btn btn-outline-light text-uppercase" href="#discover"
          >Discover</a
        >
      </div>
    </div>

    <!-- Image Slider -->
  </div>
</header>
```

We added a custom class of header for any custom styling. We are using the `py-7` class to add padding to the top and bottom of the header. We are also using the `vh-100` class to make the header take up the entire viewport height.

We are using a row with a full width column. I also added the class of `text-container` to the column for custom styling.

I added the class of `w-75` and `m-auto` to the paragraph to make it 75% of the width of the parent and center it. It looks better than the text stretching across the entire width of the screen. However, on small screens, I do want it to be full width and I want the text to be smaller, so let's add the following to the `scss/styles.scss` file:

```scss
@media (max-width: 992px) {
  // ...

  .header .text-container p {
    width: 100% !important;
    font-size: 16px;
  }
}
```

### Background Image & Sizing

We need to add a texture background image to the header with an overlay. Open the `scss/styles.scss` file and add the following code:

```scss
// Header
.header {
  background: linear-gradient(
      to bottom right,
      rgba(0, 0, 0, 0.8),
      rgba(0, 0, 0, 0.8)
    ), url('../images/header-background.jpg') center center no-repeat;
  background-size: cover;
  min-height: 1000px;
}
```

We are using the `linear-gradient` function to add an overlay to the background image. We are using the `rgba` function to add a black color with an opacity of 0.8. We are also using the `background-size` property to make sure the background image covers the entire header.

I also added a `min-height` of 1000px to the header so that if the browser height is less than 1000px, the header will still take up 1000px.

### Mobile Navbar Background

One issue that we have now is that when we make the screen smaller, the text in the navbar is hard to read. We need to add a background color to the navbar when the screen is smaller. Open the `scss/styles.scss` file and add the following code:

```scss
@media (max-width: 992px) {
  //...

  .navbar {
    background-color: #333;
  }
}
```

We will be adding an effect where on larger screens, when we scroll, the navbar will have a background color.

Here is what the header looks like now:

<img src="./images/header.png" />
