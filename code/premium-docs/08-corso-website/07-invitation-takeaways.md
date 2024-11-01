# Invitation & Takeaways Sections

We will now add a simple image with an overlay and some text for the invitation and then a couple rows of cards for the takeaways.

## Invitation

Add the following section to the `index.html` file:

```html
<!-- Invitation -->
<div class="invitation mb-5 bg-light">
  <div class="container">
    <div class="row">
      <div class="col-12">
        <div class="invitation-bg text-center py-6 rounded-5">
          <div class="text-white w-75 m-auto">
            <h2 class="display-5 fw-bold">Join Us on December 22nd</h2>
            <p>
              We cordially invite you to attend a seminar on December 22nd,
              where we will explore various topics and insights related to
              <strong>advertising and marketing</strong>. It will be an engaging
              session where you can gain valuable knowledge about. Don't miss
              out on this opportunity to enhance your skills and broaden your
              horizons. Join us and be a part of this enriching experience!
            </p>
            <a class="btn btn-primary btn-lg" href="#register">Register Now</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

### Background Image

We need to add a bit of custom CSS for the background image. Open the `scss/styles.scss` file and add the following:

```scss
// Invitation
.invitation-bg {
  background: linear-gradient(
      to bottom right,
      rgba(0, 0, 0, 0.8),
      rgba(0, 0, 0, 0.8)
    ), url('../images/invitation-background.jpg') center center no-repeat;
  background-size: cover;
}
```

Now you should see the background image with the overlay. We did the overlay by adding a gradient to the background image.

## Takeaways

Now we will do the takeaways section. Let's add a heading at the top and then some cards with icons and text.

Add the following section to the `index.html` file:

```html
<!-- Takeaways -->
<section id="takeaways" class="takeaways my-5 bg-light">
  <div class="container">
    <div class="row text-center mb-5">
      <div class="col-md-8 offset-md-2">
        <h2 class="text-center">Key Takeaways</h2>
        <p class="lead">
          Here are some of the takeaways and benefits you can expect from our
          programs.
        </p>
      </div>
    </div>

    <div class="row">
      <div class="col-md-4">
        <div class="card mb-4 rounded-0 border-0 p-3">
          <div class="card-body text-center">
            <i
              class="fas fa-atom fa-3x text-primary bg-light rounded-circle p-3 my-4"
            ></i>
            <h5 class="card-title">Scientific Insights</h5>
            <p class="card-text">
              Explore the latest scientific research and gain valuable insights
              into various subjects, from physics to biology.
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card mb-4 rounded-0 border-0 p-3">
          <div class="card-body text-center">
            <i
              class="fas fa-key fa-3x text-primary bg-light rounded-circle p-3 my-4"
            ></i>
            <h5 class="card-title">Cybersecurity Awareness</h5>
            <p class="card-text">
              Discover the importance of cybersecurity and learn how to protect
              yourself and your digital assets from cyber threats.
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card mb-4 rounded-0 border-0 p-3">
          <div class="card-body text-center">
            <i
              class="fas fa-newspaper fa-3x text-primary bg-light rounded-circle p-3 my-4"
            ></i>
            <h5 class="card-title">Industry Updates</h5>
            <p class="card-text">
              Stay informed about the latest news and updates in your industry,
              keeping you ahead of the curve and facilitating professional
              growth.
            </p>
          </div>
        </div>
      </div>

      <!-- Second Row -->
      <div class="col-md-4">
        <div class="card mb-4 rounded-0 border-0 p-3">
          <div class="card-body text-center">
            <i
              class="fas fa-users fa-3x text-primary bg-light rounded-circle p-3 my-4"
            ></i>
            <h5 class="card-title">Collaborative Networking</h5>
            <p class="card-text">
              Connect with professionals from diverse backgrounds and industries
              to foster collaboration and expand your professional network.
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card mb-4 rounded-0 border-0 p-3">
          <div class="card-body text-center">
            <i
              class="fas fa-handshake fa-3x text-primary bg-light rounded-circle p-3 my-4"
            ></i>
            <h5 class="card-title">Partnership Opportunities</h5>
            <p class="card-text">
              Discover potential partnership opportunities with like-minded
              individuals and organizations, opening doors to new collaborations
              and ventures.
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <div class="card mb-4 rounded-0 border-0 p-3">
          <div class="card-body text-center">
            <i
              class="fas fa-chart-bar fa-3x text-primary bg-light rounded-circle p-3 my-4"
            ></i>
            <h5 class="card-title">Data-driven Insights</h5>
            <p class="card-text">
              Leverage data analytics to gain valuable insights and make
              informed decisions, unlocking new possibilities for growth and
              success.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

For the heading, we used an 8 column offset by 2 columns. This will center the heading and the paragraph but it won't be as wide as the container.

Then we just added some columns and added some cards with icons with a circle background.

Here is what it looks like:

<img src="./images/takeaways.png" />
