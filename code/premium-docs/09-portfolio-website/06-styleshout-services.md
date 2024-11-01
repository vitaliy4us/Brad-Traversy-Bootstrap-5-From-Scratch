# StyleShout & Services Sections

We are going to add a section with some text as a shoutout to [Styleshout](https://styleshout.com), which is the website that we used for the inspiration of this design. Check them out if you are looking for pre-made themes. We will start with that. We will also add the services section with a backgound image and overlay similar to the header.

## Styleshout Section

Add the following code to the `index.html` file:

```html
<!-- Styleshout -->
<section class="styleshout text-bg-dark bg-gradient p-6 text-center">
  <div class="container">
    <div class="row">
      <div class="col-12">
        <h1>Shoutout to Styleshout</h1>
        <hr class="w-25 mx-auto" />
        <p class="lead mb-5">
          Styleshout is a place for Free HTML5 Templates and Free Wordpress.
          This design was inspired by one of their templates. Check them out for
          templates to use and get inspiration from.
        </p>

        <a
          href="https://styleshout.com"
          target="_blank"
          class="btn btn-primary btn-lg text-uppercase px-5 mx-3 my-2"
          >Visit Styleshout</a
        >
      </div>
    </div>
  </div>
</section>
```

This is very simple. It is a one column row with some text and a large button. We also used the `bg-gradient` class to add a gradient background.

## Services Section

Now we will create the services section, which will be a 3 column row with an icon, a title and a description. We will also have an overlay much like we did with the header. Add the following code to the `index.html` file:

```html
<!-- Services -->
<section class="services text-bg-dark py-5 position-relative">
  <div class="container">
    <div class="text-center mb-5">
      <h4 class="text-uppercase fw-bold text-primary">Services</h4>
      <hr class="w-25 mx-auto" />

      <h2 class="mb-4">What Can I Do For You?</h2>
      <p class="lead">
        Here are some of the services that I offer when it comes to web
        development and business.
      </p>
    </div>
    <div class="row">
      <div class="col-md-4 text-center">
        <i class="fas fa-globe fa-3x text-primary mb-3"></i>
        <h3 class="fs-3">Web Design</h3>
        <hr class="w-25 mx-auto" />
        <p class="fs-5">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Incidunt
          repellat rerum repudiandae soluta omnis enim quam earum vero
          repellendus quibusdam quis alias suscipit.
        </p>
      </div>

      <div class="col-md-4 text-center">
        <i class="fas fa-code fa-3x text-primary mb-3"></i>
        <h3 class="fs-3">Web Development</h3>
        <hr class="w-25 mx-auto" />
        <p class="fs-5">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Incidunt
          repellat rerum repudiandae soluta omnis enim quam earum vero
          repellendus quibusdam quis alias suscipit.
        </p>
      </div>

      <div class="col-md-4 text-center">
        <i class="fas fa-shopping-cart fa-3x text-primary mb-3"></i>
        <h3 class="fs-3">Advertising & SEO</h3>
        <hr class="w-25 mx-auto" />
        <p class="fs-5">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Incidunt
          repellat rerum repudiandae soluta omnis enim quam earum vero
          repellendus quibusdam quis alias suscipit.
        </p>
      </div>
    </div>
  </div>
</section>
```

We positioned it relative so the overlay can be positioned absolute within it. Let's add the following to the `scss/styles.scss` file:

```scss
// Services
.services {
  background: url(../images/bg.jpg) no-repeat center bottom;
  background-size: cover;
  background-attachment: fixed;
}

// Services Overlay
.services::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
}

.services .container {
  position: relative;
  z-index: 10;
}
```

We added the background image and positioning. We used the `::after` pseudo element to add the overlay. We also added a `z-index` to the container so it is on top of the overlay.


