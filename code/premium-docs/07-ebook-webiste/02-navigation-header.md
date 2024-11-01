# Navigation & Header

Up to this point, you should have your `ebook-website` project folder open in VS Code. If not, open it now. It is the `bs-5-simple-starter` that we created along with some extra images and a favicon for the website.

in this lesson, we will create the navigation, which will be fixed to the top and as we scroll, it will stay at the top. This is a common feature in modern websites. We also want to add some styles on scroll, so we will have to add a bit of custom JS for that, but it's not bad at all.

Let's start with the main navigation html:

```html
<!-- Navigation -->
<nav class="navbar navbar-expand-lg fixed-top navbar-dark">
  <div class="container">
    <a class="navbar-brand" href="#">
      <img src="images/logo.png" alt="" width="225" />
    </a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#navbarNavDropdown"
      aria-controls="navbarNavDropdown"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavDropdown">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item">
          <a class="nav-link fw-semibold" aria-current="page" href="/#home"
            >Home</a
          >
        </li>
        <li class="nav-item">
          <a class="nav-link fw-semibold" href="/#description">Details</a>
        </li>
        <li class="nav-item">
          <a
            class="nav-link btn btn-outline-light fw-semibold px-4 mx-4"
            href="contact.html"
            >Contact</a
          >
        </li>
      </ul>
    </div>
  </div>
</nav>
```

Notice I did not add a background color. That is because we will haver a background image for the header and we want the navigation to be transparent. We will add a background color on scroll, but we will do that with JS. For now, just so we can see the navigation, let's add the class `bg-dark` to the navigation:

```html
<nav class="navbar navbar-expand-lg fixed-top navbar-dark bg-dark">...</nav>
```

As you can see, we have a couple links and a contact button, which will go to a separate page later.

I do want the contact button text to be dark on hover, so add this to your `scss/style.scss` file:

```scss
.navbar .btn-outline-light:hover {
  color: #333;
}
```

We want the Home link to bring us to the top of the page, so let's add an id of `home` to the `<body>` tag:

```html
<body id="home">
  ...
</body>
```

## Header / Hero

The header will be the first thing we see when we land on the page. It will have a background image, a foreground image, some text and a form with an email input. Let's add the html for the header:

```html
<header class="header">
  <!-- Hero -->
  <div class="hero text-white pt-7">
    <div class="container-xl">
      <div class="row">
        <div class="col-lg-6">
          <div class="image-container mb-5 px-4">
            <img
              class="img-fluid"
              src="images/header-ebook.png"
              alt="alternative"
            />
          </div>
        </div>
        <div class="col-lg-6">
          <div
            class="text-container p-4 d-flex flex-column justify-content-center h-100 mb-5"
          >
            <h1 class="display-3 fw-bold">Welcome to Blog Mastery</h1>
            <p class="lead">
              Are you ready to take your blogging journey to new heights? Blog
              Mastery is your ultimate guide to creating and managing a
              successful blog that captivates your audience and drives
              engagement.
            </p>

            <!--  Form -->
            <div class="form-container text-center">
              <form>
                <div class="my-4">
                  <input
                    type="email"
                    class="form-control form-control-lg rounded-5"
                    placeholder="Email Address"
                    required
                  />
                </div>
                <div class="d-grid">
                  <button
                    type="submit"
                    class="btn btn-primary btn-lg text-white"
                  >
                    Free Download
                  </button>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</header>
```

## Header Background Image

Before we go over the html, let's add the custom background image. Open your `scss/style.scss` file and add the following:

```scss
// Header
.header {
  background: linear-gradient(rgba(0, 0, 0, 0), rgba(0, 0, 0, 0)),
    url(../images/header-background.jpg) center center no-repeat;
  background-size: cover;
}
```

Now you can remove the `bg-dark` class from the navigation. We will add a background color on scroll later.

Here we have a `<header>` tag with a `hero` div inside it. In the hero is a container, to keep everything contained. Notice that I used `container-xl`. That's because I wanted it to have a 100% width on all screen sizes but mobile. Otherwise, it looks really squished together when the browser is at certain sizes.

We are also using the Bootstrap grid system, which we will use a lot in this course. We have a row and then 2 columns that are even on large screens. On smaller screens, they will stack on top of each other.

The first column has an `image-container` div with some margin and padding. It's up to you if you want to have containers like this. We could have done without it and just put the margin and padding on the column div directly. We will do it that way as well in other projects. The second column has some text and a simple form that are all wrapped in a `text-container` div. The form itself has a `form-container` div around it. This is just to make it easier to style and to be more descriptive with our classes.

One thing to notice is on the `text-container` div, I used `d-flex`, which turns it into a flex container. I also used `flex-column` to make it a column instead of a row. Because I want them vertical. I also used `justify-content-center` to center the content vertically. This is a very common pattern in Bootstrap. You will see it a lot.

For the submit button, I wrapped it in the class of `d-grid` just because that makes it a block button that spans 100% of it's container.

## SVG Waves

I wanted to give this header/hero a cool looking border background with some waves. So right above the ending `</header>` tag, add this `svg`:

```html
<svg
  class="frame-decoration"
  data-name="Layer 2"
  xmlns="http://www.w3.org/2000/svg"
  preserveAspectRatio="none"
  viewBox="0 0 1920 192.275"
>
  <defs>
    <style>
      .cls-1 {
        fill: #f3f6f9;
      }
    </style>
  </defs>
  <title>frame-decoration</title>
  <path
    class="cls-1"
    d="M0,158.755s63.9,52.163,179.472,50.736c121.494-1.5,185.839-49.738,305.984-49.733,109.21,0,181.491,51.733,300.537,50.233,123.941-1.562,225.214-50.126,390.43-50.374,123.821-.185,353.982,58.374,458.976,56.373,217.907-4.153,284.6-57.236,284.6-57.236V351.03H0V158.755Z"
    transform="translate(0 -158.755)"
  />
</svg>
```

Now you will see a wave effect.

## Media Query

It looks great on larger screens, however, if you make the screen smaller, the image is not in the middle. So let's add a media query to fix that. Add this to your `style.scss` file:

```scss
@media (max-width: 1000px) {
  .hero .image-container {
    display: flex;
    justify-content: center;
  }

  .hero .text-container {
    text-align: center;
  }
}
```

We are now centering the image container and the text container on smaller screens.

On small screens, it may look weird when you open the hamburger menu because the menu is transparent. Let's make it so on small screens, the menu has a dark background. We will add this to our media query:

```scss
@media (max-width: 1000px) {
  // ...

  .navbar {
    background: var(--bs-dark);
  }
}
```

Notice I am using a CSS variable for the background color. This is a variable that Bootstrap provides for the dark color.

That should do it for the navigation and header part of the site. We will add the scroll effect later.
