# Contact Page

We are going to have an inner page for contact to switch it up a bit. Let's create a new file called `contact.html`. We can copy the `<head>` as well as the navigation and footer, including the social icon section. It should look like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,400;0,600;0,700;1,400&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="css/font-awesome.css" />
    <link rel="stylesheet" href="css/bootstrap.css" />
    <link rel="stylesheet" href="css/styles.css" />
    <link rel="icon" href="images/favicon.png" />
    <title>Free E-Book | Start Your Own Blog</title>
  </head>
  <body id="home">
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg fixed-top navbar-dark">
      <div class="container">
        <a class="navbar-brand" href="/index.html">
          <img src="images/logo.svg" alt="" width="124" />
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
              <a class="nav-link fw-semibold" href="/#details">Details</a>
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

    <!-- Social -->
    <section class="social text-bg-dark py-6 overflow-hidden">
      <div class="row">
        <div class="col-6 offset-3 text-center fs-4">
          <p>
            Stay connected and join our vibrant community. For any inquiries or
            assistance, feel free to reach out to us
          </p>
          <div class="social d-flex justify-content-center gap-4">
            <i class="fab fa-facebook fa-2x"></i>
            <i class="fab fa-twitter fa-2x"></i>
            <i class="fab fa-instagram fa-2x"></i>
            <i class="fab fa-linkedin fa-2x"></i>
            <i class="fab fa-pinterest fa-2x"></i>
          </div>
        </div>
      </div>
    </section>

    <footer class="border-top border-primary bg-dark text-white py-4">
      <div class="container">
        <div class="row">
          <div class="col-md-8">
            <ul class="nav">
              <li class="nav-item">
                <a class="nav-link link-light" href="/#details">Details</a>
              </li>
              <li class="nav-item">
                <a class="nav-link link-light" href="/contact.html">Contact</a>
              </li>
              <li class="nav-item">
                <a class="nav-link link-light" href="#">Terms</a>
              </li>
            </ul>
          </div>
          <div class="col-md-4">
            <p class="text-end d-none d-md-block">
              Copyright &copy; Blog Mastery 2023
            </p>
          </div>
        </div>
      </div>
    </footer>

    <script src="js/bootstrap.bundle.min.js"></script>
    <script src="js/script.js"></script>
  </body>
</html>
```

## Header

We will have a header on this and all other inner pages, but it will just be a heading. We can also use the `svg` with the waves.

Add the following right below the `nav`:

```html
<!-- Header -->
<header class="header">
  <!-- Heading -->
  <section class="text-white pt-7 pb-4">
    <div class="container">
      <div class="row">
        <div class="col-lg-12">
          <h1>Contact Information</h1>
        </div>
      </div>
    </div>
  </section>
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
</header>
```

## Contact Form

Add the following under the contact form:

```html
<!-- Contact Form -->
<section class="contact bg-light pb-4">
  <div class="container">
    <div class="row">
      <div class="col-12">
       <form>
          <div class="mb-3">
            <input
              type="text"
              class="form-control form-control-lg"
              name="name"
              placeholder="Name"
            />
          </div>
          <div class="mb-3">
            <input
              type="email"
              class="form-control form-control-lg"
              name="email"
              placeholder="Email"
            />
          </div>
          <div class="mb-3">
            <textarea
              class="form-control form-control-lg"
              name="message"
              rows="6"
              placeholder="Message"></textarea>
          </div>
          <div class="d-grid">
            <button type="submit" class="btn btn-primary text-white mt-3">
              Submit
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
</section>
```

Make sure that you add the `name` attributes because we will be deploying to Vercel and using Formspree and it uses these name attributes.

## Map

We are also going to embed a map using Google Maps. We can use the `iframe` tag to do this. We will also have some text above it:

```html
<!-- Map -->
<section class="map my-5">
  <div class="container">
    <div class="row">
      <div class="col-10 offset-1">
        <h3>Our Location</h3>
        <p class="mb-4">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit nulla
          doloremque minus ipsa, obcaecati numquam ea rerum corporis ducimus ex
          voluptate cupiditate aut excepturi necessitatibus, neque eius illum ab
          repellendus.
        </p>
        <div class="map">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1241.5303553091994!2d-0.14076024298621118!3d51.51210217963597!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487604d502268421%3A0x6a7d62889992f993!2sRegent+St%2C+Soho%2C+London+W1B+5TH%2C+UK!5e0!3m2!1sen!2sro!4v1476174541049"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</section>
```

We need to size the map, so in the `scss/styles.scss`, add the following:

```scss
.map iframe {
  left: 0;
  top: 0;
  height: 400px;
  width: 100%;
  border: none;
}
```

That's it! We have our ebook website complete.

The form doesn't work, however, in the next video I am going to show you how we can deploy this website to Vercel and hook up the form with a service called `Formspree`.
