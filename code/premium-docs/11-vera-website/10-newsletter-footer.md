# Newsletter & Footer

We will have a small newsletter subscribe form at the bottom of the page. Add the following code to your `index.html` file:

```html
<!-- Newsletter -->
<section id="newsletter" class="newsletter my-6">
  <div class="container">
    <div class="row mb-4">
      <div
        class="col-md-6 offset-md-3 d-flex flex-column align-items-center text-center"
      >
        <h2 class="fw-bold">Subscribe And Follow</h2>
        <p>
          Stay updated with our latest news and announcements. Subscribe to our
          newsletter and follow us on social media for valuable insights and
          exciting updates.
        </p>
      </div>
    </div>
    <div class="row">
      <div
        class="col-md-6 offset-md-3 d-flex flex-column align-items-center text-center"
      >
        <div class="input-group mb-3">
          <input
            type="text"
            class="form-control"
            placeholder="Enter Email Address"
            aria-label="Recipient's username"
            aria-describedby="button-addon2"
          />
          <button class="btn btn-primary text-white rounded-0" type="button">
            Submit
          </button>
        </div>
      </div>
    </div>
  </div>
</section>
```

We have a heading and then an input group with an email input and a button.

## Footer

The footer will be really simple and almost identical to the Yavin project footer. Add the following code to your `index.html` file:

```html
<!-- Footer -->
<footer class="footer bg-secondary py-6">
  <div class="container">
    <div class="row">
      <div class="col-md-4 my-3">
        <h6>About Vera</h6>
        <p>
          Vera is a dedicated software solutions company that aims to provide
          exceptional services to its clients. We are committed to delivering
          innovative and customized solutions that meet your specific business
          needs.
        </p>
      </div>
      <div class="col-md-4 my-3">
        <h6>Links</h6>
        <ul class="list-unstyled">
          <li>
            Important: <a href="#">Terms & Conditions</a>,
            <a href="privacy.html">Privacy Policy</a>
          </li>
          <li>
            Useful: <a href="/#expertise">Expertise</a>,
            <a href="/#pricinf">Pricing</a>,
            <a href="/#newsletter">Newsletter</a>
          </li>
          <li>
            Menu: <a href="#home">Home</a>, <a href="/#details">Details</a>,
            <a href="/#solutions">Solutions</a>,
            <a href="/#projects">Projects</a>
          </li>
        </ul>
      </div>
      <div class="col-md-4 my-3">
        <div class="mb-4">
          <a href="#" class="text-decoration-none">
            <i class="fab fa-facebook fa-3x text-light mx-2"></i>
          </a>
          <a href="#" class="text-decoration-none">
            <i class="fab fa-twitter fa-3x text-light mx-2"></i>
          </a>
          <a href="#" class="text-decoration-none">
            <i class="fab fa-instagram fa-3x text-light mx-2"></i>
          </a>
          <a href="#" class="text-decoration-none">
            <i class="fab fa-pinterest fa-3x text-light mx-2"></i>
          </a>
        </div>
        <p>
          We would love to hear from you
          <a href="mailto:contact@site.com"
            ><strong>contact@site.com</strong></a
          >
        </p>
      </div>
    </div>
  </div>
</footer>
```

It has an about section, some links and some social icons. I want to have an inner page as well, so you can see the privacy link goes to `privacy.html`. We will add that in the next lesson.
