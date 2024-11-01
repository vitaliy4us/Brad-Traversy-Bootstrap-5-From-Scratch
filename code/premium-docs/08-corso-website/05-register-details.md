# Register & Details Sections

We will have a register section with some content as well as a form. We will create the first of 2 details sections, which are just images and text.

## The Register Section

Add the following code to the `index.html` file:

```html
<!-- Register -->
<section id="register" class="register bg-primary py-6 overflow-hidden">
  <div class="container">
    <div class="row">
      <div class="col-lg-6">
        <h2>Unlock Your Potential with Engaging Content</h2>
        <p>
          Our wide range of training and seminar videos are designed to empower
          you with valuable knowledge and skills.
        </p>
        <ul class="list-unstyled vstack gap-3">
          <li>
            <i class="fas fa-square"></i>
            <strong>Gain Expertise:</strong> Our videos provide in-depth
            insights and practical tips to enhance your expertise in various
            domains.
          </li>
          <li>
            <i class="fas fa-square"></i>
            <strong>Stay Updated:</strong> Stay up-to-date with the latest
            industry trends and advancements through our informative and
            up-to-date videos.
          </li>
          <li>
            <i class="fas fa-square"></i>
            <strong>Expand Your Network:</strong> Connect with like-minded
            individuals and industry experts, fostering new connections and
            opportunities.
          </li>
        </ul>
      </div>
      <div class="col-lg-6 p-4">
        <form>
          <div class="my-4">
            <input
              type="text"
              class="form-control form-control-lg rounded-0 border-0"
              placeholder="Enter name"
            />
          </div>
          <div class="my-4">
            <input
              type="email"
              class="form-control form-control-lg rounded-0 border-0"
              placeholder="Enter email"
            />
          </div>
          <div class="my-4">
            <input
              type="text"
              class="form-control form-control-lg rounded-0 border-0"
              placeholder="Enter phone number"
            />
          </div>
          <div class="form-check">
            <input class="form-check-input" type="checkbox" value="" />
            <label class="form-check-label" for="flexCheckIndeterminate">
              I agree to the terms and conditions
            </label>
          </div>
          <div class="d-grid mt-4">
            <button class="btn btn-outline-dark">Register</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</section>
```

We add a class of `overflow-hidden` to prevent any content from overflowing outside of the section. We also add a class of `py-6` to add some padding to the top and bottom of the section.

For the unordered list spacing, I used the `vstack` class with a gap of 3. Then we have the form on the right side.

On small screens, I want to lessen the top and bottom padding and also align the heading to the center. So add the following code to the `scss/style.scss` file:

```scss
@media (max-width: 992px) {
  // ...

  .register {
    padding: 40px 0 !important;
  }

  .register h2 {
    text-align: center;
  }
}
```

## The Details Section

The details section is easy, add the following code to the `index.html` file:

```html
<!-- Details 1 -->
<section id="discover" class="details py-6 bg-light">
  <div class="container">
    <div class="row">
      <div class="col-lg-6">
        <img
          class="img-fluid rounded-5 mb-4"
          src="images/instructor.jpg"
          alt=""
        />
      </div>
      <div class="col-lg-6 d-flex flex-column justify-content-center">
        <h2>Enhance Your Skills with Engaging Training Videos</h2>
        <p>
          Our extensive collection of training videos is designed to help you
          enhance your skills and excel in your chosen field. Whether you're
          looking to improve your technical expertise or develop essential soft
          skills, our videos provide valuable insights and practical knowledge.
        </p>
        <p>
          With expert instructors and comprehensive content, you'll gain the
          confidence and competence to tackle challenges and achieve success.
        </p>
      </div>
    </div>
  </div>
</section>
```

We are using the `bg-light` class for the background color. We also have a class of `py-6` for padding on the top and bottom. We have a row with 2 columns. The first column has an image and the second column has the text.

For the text, I wanted to align it in the center vertically. That's why I made it a flex box and used the `justify-content-center` class.

Here is what it looks like:

<img src="./images/register.png" />
