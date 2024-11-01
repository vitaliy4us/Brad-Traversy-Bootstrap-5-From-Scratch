# Video Modal

Now we want to be able to click on the video image and open the video in a modal. We will be adding a little custom JS for this.

Start by adding the modal html. I am going to put it right in the video section from last lesson:

```html
<!-- Video -->
<section class="video my-6">
  <div class="container">
    <div class="row">
      <div class="col-lg-12 d-flex flex-column align-items-center">
        <div class="position-relative">
          <img
            class="img-fluid"
            src="images/video-preview.jpg"
            alt=""
          />
          <a
            class="video-btn"
            data-bs-toggle="modal"
            data-bs-target="#videoModal"
            data-bs-src="https://www.youtube.com/embed/u72H_zZzkcw"
          >
            <span class="video-play-button">
              <span></span>
            </span>
          </a>
        </div>
      </div>
    </div>
    <div class="video-points row px-6 mt-5">
      <div class="col-lg-4">
        <h4 class="fw-bold">10 Years Of Experience</h4>
        <p>
          Felis eget lectus consequat rutrum suspendi felis elit, interdum at
          eros eget valomre
        </p>
      </div>
      <div class="col-lg-4">
        <h4 class="fw-bold">Enduring Partnerships</h4>
        <p>
          Felis eget lectus consequat rutrum suspendi felis elit, interdum at
          eros eget valomre
        </p>
      </div>
      <div class="col-lg-4">
        <h4 class="fw-bold">Skilled Capable Team</h4>
        <p>
          Felis eget lectus consequat rutrum suspendi felis elit, interdum at
          eros eget valomre
        </p>
      </div>
    </div>
  </div>

  <!-- Video Modal (ADD THIS) -->
  <div class="video-modal">
    <div
      class="modal fade"
      id="videoModal"
      tabindex="-1"
      role="dialog"
      aria-hidden="true"
    >
      <div class="modal-dialog" role="document">
        <div class="modal-content">     
          <div class="ratio ratio-16x9">
            <iframe
              class="embed-responsive-item"
              id="video"
              allow="autoplay"
            ></iframe>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
```

## Custom Styles

We need to add a few styles for the sizing and positioning of the modal. Open the `css/styles.css` file and add the following:

```css
.video-modal .modal-dialog {
  max-width: 1150px;
  margin-top: 200px;
}
```

This will now open a modal, however it will be blank. We need to add some JS to make it work. Open the `js/scripts.js` file and add the following:

```js
// Video Modal
const videoBtn = document.querySelector('.video-btn');
const videoModal = document.querySelector('#videoModal');
const video = document.querySelector('#video');
let videoSrc;

if (videoBtn !== null) {
  videoBtn.addEventListener('click', function (e) {
    videoSrc = videoBtn.getAttribute('data-bs-src');
  });
}


if (videoModal !== null) {
  videoModal.addEventListener('shown.bs.modal', (e) => {
    video.setAttribute(
      'src',
      videoSrc + '?autoplay=1&amp;modestbranding=1&amp;showinfo=0'
    );
  });

  videoModal.addEventListener('hide.bs.modal', (e) => {
    video.setAttribute('src', videoSrc);
  });
}
```

Here, we are getting the video source from the `data-bs-src` attribute on the `a` tag. Then we are adding that source to the `src` attribute on the `iframe` tag in the modal. We are also adding some query parameters to the end of the source to autoplay the video and hide the YouTube branding.

Now, try and click on the video image and you should see my YouTube video play. Of course, you can make this any video by changing the link.
