# Details & Expertise

We have two details areas with images and text and then we have the expertise icon area.

## Details

We will have 2 details sections, which will be 2 columns each with text on one side and an image on the other. We will rotate the image on the second section. Let's add the following code to the bottom of the `index.html` file:

```html
<!-- Details 1 -->
    <section id="details" class="details my-5 position-relative">
      <div class="container">
        <div class="row pt-5">
          <div class="col-lg-6">
            <h2 class="fw-bold">Evaluation And Deployment</h2>
            <hr class="hr-heading" />
            <p>
              We offer comprehensive evaluation and deployment services to ensure a smooth and successful implementation of our software solutions.</a>
            </p>
            <ul class="list-unstyled lh-lg">
              <li class="d-flex align-items-center">
            <i class="fas fa-check text-primary mx-3"></i>
            <div>
              <strong>Customized Solutions:</strong> We tailor our solutions to align with your unique business needs
            </div>
          </li>
          <li class="d-flex align-items-center">
            <i class="fas fa-check text-primary mx-3"></i>
            <div>
              <strong>Seamless Integration:</strong> Our team ensures smooth integration of the software into your existing infrastructure, minimizing disruptions
            </div>
          </li>
            </ul>
          </div>
          <div class="col-lg-6">
            <img
              class="img-fluid rounded-2"
              src="images/details-1.jpg"
              alt=""
            />
          </div>
        </div>
      </div>
      <img
        class="vertical-decoration position-absolute d-none d-md-block"
        src="images/vertical-decoration-left.svg"
        alt=""
      />
    </section>

    <!-- Details 2 -->
    <section class="details-2 my-6 position-relative">
      <div class="container">
        <div class="row pt-5">
          <div class="col-lg-6">
            <img
              class="img-fluid rounded-2 mb-3"
              src="images/details-2.jpg"
              alt=""
            />
          </div>
          <div class="col-lg-6">
            <h2 class="fw-bold">Maintenance And Support Services</h2>
            <hr class="hr-heading" />
            <p>
               We provide comprehensive maintenance and support services to ensure the smooth and uninterrupted operation of your software solutions.
    <a href="#">Learn more about our support services.</a>
            </p>
            <ul class="list-unstyled lh-lg">
             <li class="d-flex align-items-center">
      <i class="fas fa-check text-primary mx-3"></i>
      <div>
        <strong>Proactive Maintenance:</strong> We proactively monitor and maintain your software solutions to prevent issues and optimize performance.
      </div>
    </li>
    <li class="d-flex align-items-center">
      <i class="fas fa-check text-primary mx-3"></i>
      <div>
        <strong>Timely Updates:</strong> We ensure your software is up to date with the latest features, security patches, and enhancements.
      </div>
    </li>

            </ul>
          </div>
        </div>
      </div>
      <img
        class="vertical-decoration position-absolute d-none d-md-block"
        src="images/vertical-decoration-right.svg"
        alt=""
      />
    </section>
```

We have to position the background decoration images. Add the following to the `scss/styles.scss` file:

```scss
.details .vertical-decoration {
  top: 0;
  left: 0;
  width: 24px;
}

.details-2 .vertical-decoration {
  top: 5%;
  right: 0;
  width: 24px;
}
```

This part of the page should look like this:

<img src="./images/vera5.png">

## Expertise

Expertise will be some cards with icons and text. Let's add the following code to the bottom of the `index.html` file:

```html
<!-- Expertise -->
<section id="expertise" class="expertise bg-secondary my-6 py-5">
  <div class="container">
    <!-- Heading -->
    <div class="row mb-4">
      <div
        class="col-md-6 offset-md-3 d-flex flex-column align-items-center text-center"
      >
        <h5>
          <span class="badge bg-primary rounded-0 text-uppercase"
            >Expertise</span
          >
        </h5>
        <h2 class="fw-bold">Expertise Strong Points</h2>
        <p>
          We take pride in our expertise. With years of experience and a
          dedicated team, we deliver exceptional software solutions tailored to
          your needs. Our strong points include:
        </p>
      </div>
    </div>
    <!-- Expertise Row 1 -->
    <div class="row">
      <div class="col-md-3">
        <div class="card bg-transparent border-0 text-center mb-3">
          <div class="card-image">
            <i class="fas fa-lightbulb fa-5x text-primary"></i>
          </div>
          <div class="card-body">
            <h4 class="card-title fs-3">Flexible Services</h4>
            <p>Morbi blandit felis at pharetra facilisis nullam necro</p>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="card bg-transparent border-0 text-center mb-3">
          <div class="card-image">
            <i class="fas fa-wifi fa-5x text-primary"></i>
          </div>
          <div class="card-body">
            <h4 class="card-title fs-3">Great Design</h4>
            <p>Morbi blandit felis at pharetra facilisis nullam necro</p>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="card bg-transparent border-0 text-center mb-3">
          <div class="card-image">
            <i class="fas fa-desktop fa-5x text-primary"></i>
          </div>
          <div class="card-body">
            <h4 class="card-title fs-3">Easy To Use</h4>
            <p>Morbi blandit felis at pharetra facilisis nullam necro</p>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="card bg-transparent border-0 text-center mb-3">
          <div class="card-image">
            <i class="fas fa-cog fa-5x text-primary"></i>
          </div>
          <div class="card-body">
            <h4 class="card-title fs-3">Smart Options</h4>
            <p>Morbi blandit felis at pharetra facilisis nullam necro</p>
          </div>
        </div>
      </div>
    </div>
    <!-- Expertise Row 2 -->
    <div class="row">
      <div class="col-md-3">
        <div class="card bg-transparent border-0 text-center mb-3">
          <div class="card-image">
            <i class="fas fa-glasses fa-5x text-primary"></i>
          </div>
          <div class="card-body">
            <h4 class="card-title fs-3">Advanced Tech</h4>
            <p>Morbi blandit felis at pharetra facilisis nullam necro</p>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="card bg-transparent border-0 text-center mb-3">
          <div class="card-image">
            <i class="fas fa-graduation-cap fa-5x text-primary"></i>
          </div>
          <div class="card-body">
            <h4 class="card-title fs-3">Good Expertise</h4>
            <p>Morbi blandit felis at pharetra facilisis nullam necro</p>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="card bg-transparent border-0 text-center mb-3">
          <div class="card-image">
            <i class="fas fa-chart-bar fa-5x text-primary"></i>
          </div>
          <div class="card-body">
            <h4 class="card-title fs-3">Detailed Reports</h4>
            <p>Morbi blandit felis at pharetra facilisis nullam necro</p>
          </div>
        </div>
      </div>
      <div class="col-md-3">
        <div class="card bg-transparent border-0 text-center mb-3">
          <div class="card-image">
            <i class="fas fa-cloud fa-5x text-primary"></i>
          </div>
          <div class="card-body">
            <h4 class="card-title fs-3">Cloud Storage</h4>
            <p>Morbi blandit felis at pharetra facilisis nullam necro</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

We added another heading with a badge. We also got rid of the border and background for the cards.