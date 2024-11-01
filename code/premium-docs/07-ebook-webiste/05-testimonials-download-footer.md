# Testimonials, Download, and Footer

Let's add the last 3 sections to the page. A testimonial area with 3 columns, a download form with an email input and an image with a negative margin and a social icon area with a simple footer.

## Testimonials Section

Add the following html to the page:

```html
<!-- Testimonials -->
<div class="testimonials mb-8">
  <div class="container">
    <div class="row">
      <div class="col-md-4 text-center">
        <img
          src="https://randomuser.me/api/portraits/men/32.jpg"
          alt=""
          class="rounded-circle mb-3"
        />
        <p class="lead fst-italic">
          "This ebook completely transformed my blogging journey. The practical
          strategies and valuable insights helped me take my blog to new
          heights. I highly recommend it!"
        </p>
        <p class="fw-bold">Kenny Smith - Portland ME</p>
      </div>
      <div class="col-md-4 text-center">
        <img
          src="https://randomuser.me/api/portraits/women/32.jpg"
          alt=""
          class="rounded-circle mb-3"
        />
        <p class="lead fst-italic">
          "I'm so grateful for this ebook! It provided me with the guidance and
          inspiration I needed to create engaging content and build a loyal
          readership. It's a game-changer!"
        </p>
        <p class="fw-bold">Laurie Mitchell - Miami FL</p>
      </div>
      <div class="col-md-4 text-center">
        <img
          src="https://randomuser.me/api/portraits/men/31.jpg"
          alt=""
          class="rounded-circle mb-3"
        />
        <p class="lead fst-italic">
          "I can't recommend this ebook enough. It's a treasure of blogging
          wisdom. It helped me unlock my creativity, connect with my audience,
          and achieve remarkable results."
        </p>
        <p class="fw-bold">Henry White - Boston MA</p>
      </div>
    </div>
  </div>
</div>
```

This is very simple. We just added an image from the randomuser.me API, a paragraph with a quote, and a paragraph with the name and location of the person who said the quote.

## Download Section

Let's add the download section:

```html
<!-- Download -->
<section class="download">
  <div class="container">
    <div class="row">
      <div class="col-lg-5">
        <div class="image-container mt-n6 mb-5">
          <img
            class="img-fluid"
            src="images/download-ebook.png"
            alt="alternative"
          />
        </div>
      </div>
      <div class="col-lg-7">
        <div
          class="text-container text-white d-flex flex-column justify-content-center h-100 mb-5"
        >
          <h2 class="fw-bold">Get Your Free Ebook Now</h2>
          <p>
            Unlock the power of knowledge and take your blogging journey to the
            next level. Our ebook, "Blog Mastery: The Ultimate Guide to Blogging
            Success," is your key to success.
          </p>

          <!--  Form -->
          <form>
            <div class="input-group mb-3">
              <input
                type="text"
                class="form-control"
                placeholder="Email Address"
              />
              <button
                class="btn btn-primary text-white rounded-end"
                type="button"
              >
                Download
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</section>
```

Notice on the image container, we add the class `mt-n6` to add a negative margin top. This will make the image overlap the section above it. However, negative margins are disabled by default. Open your `scss/bootstrap.scss` file and add the following:

```scss
$enable-negative-margins: true;
```

Now you should see the image overlapping the section above it. The rest is pretty easy. We used an input group with the email input and button.

Add the background image to this section by adding the following to the `scss/styles.scss`:

```scss
.download {
  background: url(../images/download-background.jpg) center center no-repeat;
  background-size: cover;
}
```

## Footer

The footer has 2 parts. The social media icons and then the links and copyright. Let's add the social media icons:

```html
<!-- Social -->
<section class="social text-bg-dark py-6 overflow-hidden">
  <div class="container">
    <div class="row">
      <div class="col-md-6 offset-md-3 text-center fs-4">
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
  </div>
</section>
```

Now let's add the footer:

```html
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
```

I decided to just hide the copyright on smaller screens.

Now the homepage is done. In the next lesson, we will create the contact page.
