# Details Sections With Modals & Statement Section

In this lesson, we will create the 2 details sections, which are just an image, some text and a list. It will also have a button to open a modal. The modal will basically have the same content as the details section, but it will have a button that could go to a download page, etc. We also have a statement section in between the details sections, which will be some text with a light background.

## Details Section

Let's create our first details section. Add the following html to the page:

```html
<!-- Details -->
<section id="details" class="details my-5">
  <div class="container">
    <div class="row">
      <div class="col-lg-6">
        <div
          class="text-container d-flex flex-column justify-content-center h-100"
        >
          <h2 class="display-6">Unlock Your Blogging Potential</h2>
          <p>
            Are you ready to unleash your true blogging potential? Our ebook,
            "Blog Mastery," provides you with the tools and knowledge to take
            your blog to the next level.
          </p>
          <ul class="list-group list-group-flush lh-lg">
            <li class="list-group-item">
              <i class="fas fa-square text-primary"></i>
              <strong>Unleash Your Creativity:</strong> Our ebook empowers you
              to unleash your creativity and express your unique voice through
              your blog.
            </li>
            <li class="list-group-item">
              <i class="fas fa-square text-primary"></i>
              <strong>Maximize Your Reach:</strong> Learn how to optimize your
              blog for search engines.
            </li>
            <li class="list-group-item">
              <i class="fas fa-square text-primary"></i>
              <strong>Monetization Strategies:</strong> Discover various
              monetization strategies, such as sponsored content & affiliate
              marketing.
            </li>
          </ul>
          <a
            class="btn btn-primary text-white mt-4 align-self-start"
            data-bs-toggle="modal"
            data-bs-target="#modal1"
            >Get Your Copy Now</a
          >
        </div>
      </div>
      <div class="col-lg-6">
        <div class="image-container p-5">
          <img
            class="img-fluid"
            src="images/description.png"
            alt="alternative"
          />
        </div>
      </div>
    </div>
  </div>
</section>
```

We used `d-flex` and some alignment classes on the text container to center the content vertically. We also used `h-100` to make the text container take up the full height of the column. We created a flush styled list group and increased the line height of the list items. We also added a button that will open the modal. It has the attributes `data-bs-toggle="modal"` and `data-bs-target="#modal1"`.

## Modal

Now, let's add the modal:

```html
<!-- Modal 1 -->
<div id="modal1" class="modal fade" tabindex="-1" aria-hidden="true">
  <div class="modal-dialog modal-lg mt-7">
    <div class="modal-content p-5">
      <div class="row">
        <div class="col-lg-6">
          <div class="image-container">
            <img
              class="img-fluid"
              src="images/description.png"
              alt="alternative"
            />
          </div>
          <!-- end of image-container -->
        </div>
        <!-- end of col -->
        <div class="col-lg-6">
          <div class="text-container">
            <h3 class="display-6">Unlock Your Blogging Potential</h3>
            <p>
              Are you ready to unleash your true blogging potential? Our ebook,
              "Blog Mastery," provides you with the tools and knowledge to take
              your blog to the next level.
            </p>
            <ul class="list-group list-group-flush lh-lg mb-4">
              <li class="list-group-item">
                <i class="fas fa-square text-primary"></i>
                <strong>Unleash Your Creativity:</strong> Our ebook empowers you
                to unleash your creativity and express your unique voice through
                your blog.
              </li>
              <li class="list-group-item">
                <i class="fas fa-square text-primary"></i>
                <strong>Maximize Your Reach:</strong> Learn how to optimize your
                blog for search engines.
              </li>
              <li class="list-group-item">
                <i class="fas fa-square text-primary"></i>
                <strong>Monetization Strategies:</strong> Discover various
                monetization strategies, such as sponsored content & affiliate
                marketing.
              </li>
            </ul>
            <a class="btn btn-primary text-white" href="#header"
              >Free Download</a
            >
            <button type="button" class="btn btn-light" data-bs-dismiss="modal">
              Close
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

I want the modal to be wider, so we will add the following css to the `scss/style.scss` file:

```scss
// Modal
.modal-dialog {
  max-width: 1040px;
}
```

Now, you should see the modal when you click on the button.

## Statement Section

Now we will create the statement section, which is very simple. It is a heading and paragraph with a light background. We will also create a 3 column testimonial section and a download section.

Add the following html to the page:

```html
<!-- Statement -->
<section class="statement mb-5">
  <div class="container">
    <div class="row">
      <div class="col-12">
        <div class="text-container bg-light p-5 rounded-5">
          <h2>Master the Art of Blogging Excellence</h2>
          <p>
            Transform your blog from a mere hobby to a thriving online business
            with our ebook, "Blog Mastery: Monetize Your Passion." This
            invaluable resource is your roadmap to turning your blog into a
            profitable venture. Learn how to monetize your content through
            various strategies such as sponsored posts, affiliate marketing, and
            product creation. Gain insights into building a strong brand,
            attracting lucrative partnerships, and maximizing your earning
            potential. Take the leap and unlock the financial rewards of your
            blogging journey.
          </p>
        </div>
      </div>
    </div>
  </div>
</section>
```

## Second Details Section

This details section will have different text and image in both the page content and the modal. Add the following html to the page:

```html
<section class="details my-5">
  <div class="container">
    <div class="row">
      <div class="col-lg-6">
        <div class="image-container p-5">
          <img class="img-fluid" src="images/author.png" alt="alternative" />
        </div>
      </div>
      <div class="col-lg-6">
        <div
          class="text-container d-flex flex-column justify-content-center h-100"
        >
          <h2 class="display-6">Craft Remarkable Content</h2>

          <p>
            Discover techniques for effective storytelling, engaging visuals,
            and compelling calls-to-action. Unlock the secrets of creating a
            consistent and authentic brand voice that sets you apart from the
            competition. With our ebook, you'll have the knowledge and
            inspiration to captivate your audience and leave a lasting
            impression.
          </p>
          <ul class="list-group list-group-flush lh-lg">
            <li class="list-group-item">
              <i class="fas fa-square text-primary"></i>
              <strong>Embrace Your Unique Voice:</strong> Learn how to harness
              the power of your unique voice.
            </li>
            <li class="list-group-item">
              <i class="fas fa-square text-primary"></i>
              <strong>Spark Creativity:</strong> Explore techniques to spark
              creativity and overcome writer's block.
            </li>
            <li class="list-group-item">
              <i class="fas fa-square text-primary"></i>
              <strong>Engage Your Readers:</strong> Discover strategies for
              creating content that engages your readers on a deeper level.
            </li>
          </ul>
          <a
            class="btn btn-primary text-white mt-4 align-self-start"
            data-bs-toggle="modal"
            data-bs-target="#modal2"
            >Learn More</a
          >
        </div>
      </div>
    </div>
  </div>
</section>
```

Now add the second modal:

```html
<!-- Modal 2 -->
<div id="modal2" class="modal fade" tabindex="-1" aria-hidden="true">
  <div class="modal-dialog modal-lg mt-7">
    <div class="modal-content p-5">
      <div class="row">
        <div class="col-lg-6">
          <div class="image-container">
            <img class="img-fluid" src="images/author.png" alt="alternative" />
          </div>
          <!-- end of image-container -->
        </div>
        <!-- end of col -->
        <div class="col-lg-6">
          <div class="text-container">
            <h3 class="display-6">Craft Remarkable Content</h3>

            <p>
              Discover techniques for effective storytelling, engaging visuals,
              and compelling calls-to-action. Unlock the secrets of creating a
              consistent and authentic brand voice that sets you apart from the
              competition. With our ebook, you'll have the knowledge and
              inspiration to captivate your audience and leave a lasting
              impression.
            </p>
            <ul class="list-group list-group-flush lh-lg mb-3">
              <li class="list-group-item">
                <i class="fas fa-square text-primary"></i>
                <strong>Embrace Your Unique Voice:</strong> Learn how to harness
                the power of your unique voice.
              </li>
              <li class="list-group-item">
                <i class="fas fa-square text-primary"></i>
                <strong>Spark Creativity:</strong> Explore techniques to spark
                creativity and overcome writer's block.
              </li>
              <li class="list-group-item">
                <i class="fas fa-square text-primary"></i>
                <strong>Engage Your Readers:</strong> Discover strategies for
                creating content that engages your readers on a deeper level.
              </li>
            </ul>
            <a class="btn btn-primary text-white" href="#header"
              >Free Download</a
            >
            <button type="button" class="btn btn-light" data-bs-dismiss="modal">
              Close
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```
