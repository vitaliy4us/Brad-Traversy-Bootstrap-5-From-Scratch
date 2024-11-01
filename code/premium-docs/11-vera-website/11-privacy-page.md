# Privacy Page

I wanted to have an inner page for this project. We will create a simple privacy policy page. 

This is an example of a documentation page, which could be anything from a privacy policy to terms of service to license agreements and much more.

I will create a new file called `privacy.html`. We want to copy the `head` as well as the `navbar` and `footer` from the index.html page. It should look like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap"
      rel="stylesheet"
    />
    <link rel="stylesheet" href="css/font-awesome.css" />
    <link rel="stylesheet" href="css/bootstrap.css" />
    <link rel="stylesheet" href="css/styles.css" />
    <link rel="icon" href="images/favicon.png" />
    <title>Welcome To Vera</title>
  </head>
  <body id="home">
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg sticky-top navbar-dark">
      <div class="container">
        <a class="navbar-brand" href="index.html">
          <img src="images/logo.svg" alt="" width="100" />
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
              <a class="nav-link" aria-current="page" href="index.html">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="index.html#solutions">Solutions</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="index.html#details">Details</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="index.html#expertise">Expertise</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="index.html#pricing">Pricing</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="index.html#projects">Projects</a>
            </li>
          </ul>
          <span class="nav-item">
            <span class="fa-stack">
              <a href="https://facebook.com" target="_blank">
                <i class="fas fa-circle fa-stack-2x"></i>
                <i class="fab fa-facebook-f fa-stack-1x text-white"></i>
              </a>
            </span>
            <span class="fa-stack">
              <a href="https://twitter.com" target="_blank">
                <i class="fas fa-circle fa-stack-2x"></i>
                <i class="fab fa-twitter fa-stack-1x text-white"></i>
              </a>
            </span>
          </span>
        </div>
      </div>
    </nav>

    <!-- NEW CONTENT HERE -->

    <!-- Footer -->
    <footer class="footer bg-secondary py-6">
      <div class="container">
        <div class="row">
          <div class="col-md-4 my-3">
            <h6>About Yavin</h6>
            <p class="p-small">
              He oppose at thrown desire of no. Announcing impression unaffected
              day his are unreserved indulgence. Him hard find read are you
            </p>
          </div>
          <div class="col-md-4 my-3">
            <h6>Links</h6>
            <ul class="list-unstyled li-space-lg p-small">
              <li>
                Important: <a href="#">Terms & Conditions</a>,
                <a href="#">Privacy Policy</a>
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
            <p class="p-small">
              We would love to hear from you
              <a href="mailto:contact@site.com"
                ><strong>contact@site.com</strong></a
              >
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

## Inner Page Header

The header on inner pages will be simple. It will be a row with a full column and some text. Add this code after the `navbar`:

```html
<!-- Inner Page Header -->
<header class="bg-secondary p-5">
  <div class="container">
    <div class="row">
      <div class="col-12">
        <h1 class="fw-bold">Privacy Policy</h1>
      </div>
    </div>
  </div>
</header>
```

## Privacy Policy Content

Now we will add the content of the privacy policy. The way that I will structure the content is like this:

- Main heading/topic
- Text and bullet points
- Secondary topic
- Text and bullet points

Add this code after the header:

```html
<!-- Page Content -->
    <section class="policy-content my-5">
      <div class="container">
        <div class="row">
          <div class="col-xl-10 offset-xl-1">
            <h2>1. Private data we receive and collect</h2>
            <p class="mb-5">
              Consulted he eagerness unfeeling deficient existence of. Calling
              nothing end fertile for venture way boy. Esteem spirit temper too
              say adieus who direct esteem. It esteems luckily mr or picture
              placing drawing no. Apartments frequently or motionless on
              reasonable projecting expression. Way mrs end gave tall walk fact
              bed.
            </p>
            <h4>1.1. For example each time you visit the website</h4>
            <p class="mb-5">
              Ye on properly handsome returned throwing am no whatever. In
              without wishing he of picture no exposed talking minutes.
              Curiosity continual belonging offending so explained it exquisite.
              Do remember to followed yourself material mr recurred carriage.
              High drew west we no or at john. About or given on witty event. Or
              sociable up material.
            </p>
            <h4>1.2. When you first register for a package account</h4>
            <p class="mb-5">
              Moderate children at of outweigh it. UnSociable on as carriage my
              position weddings raillery consider. Peculiar trifling absolute
              and wandered vicinity property yet. The and collecting motionless
              difficulty son. His hearing staying ten colonel met. Sex drew six
              easy four dear cold deny. satiable it considered invitation he
              found the light.
            </p>


            <h2>2. Advantages of working with service</h2>
            <p class="mb-5">
              Ye on properly handsome returned throwing am no whatever. In
              without wishing he of picture no exposed talking minutes.
              Curiosity continual belonging offending so explained it exquisite.
              Do remember to followed yourself material mr recurred carriage.
              High drew west we no or at john. About or given on witty event. Or
              sociable up material
            </p>
            <h4>2.1. For example each time you visit the website</h4>
            <p class="mb-5">
              Ye on properly handsome returned throwing am no whatever. In
              without wishing he of picture no exposed talking minutes.
              Curiosity continual belonging offending so explained it exquisite.
              Do remember to followed yourself material mr recurred carriage.
              High drew west we no or at john. About or given on witty event. Or
              sociable up material.
            </p>
            <ul class="list-unstyled mb-4 lh-lg">
              <li class="d-flex align-items-center">
                <i class="fas fa-check text-primary mx-3"></i>
                <div>
                  <strong>To story tell you</strong> moderate children at of
                  outweigh it. UnSociable on as carriage my position weddings
                  raillery consider. Peculiar trifling absolute and wandered
                  vicinity property yet
                </div>
              </li>
              <li class="d-flex align-items-center">
                <i class="fas fa-check text-primary mx-3"></i>
                <div>
                  <strong>To enable us</strong> the and collecting motionless
                  difficulty son. His hearing staying ten colonel met. Word drew
                  six easy four dear cold deny. satiable it considered
                  invitation he travelling insensible
                </div>
              </li>
              <li class="d-flex align-items-center">
                <i class="fas fa-check text-primary mx-3"></i>
                <div>
                  <strong>To verify your</strong> fulfilled direction use
                  continual set him propriety continued. Saw met applauded
                  favourite deficient engrossed concealed and her. Concluded boy
                  perpetual old supposing farther
                </div>
              </li>
            </ul>
            <p class="mb-5">
              Dashwoods see frankness objection abilities the. As hastened oh
              produced prospect formerly up am. Placing forming nay looking old
              married few has. Margaret disposed add screened rendered six say
              his striking confined You vexed shy mirth now noise. Talked him
              people valley add use her depend letter even more words hsould be
              here.
            </p>

            <h2>3. Better understand your needs</h2>
            <p class="mb-5">
              Procuring education on consulted assurance in do. Is sympathize he
              expression mr no travelling. Preference he he at travelling in
              resolution. So striking at of to welcomed resolved. Northward by
              described up household therefore attention. Excellence decisively
              nay man yet impression for contrasted remarkably. There spoke
              happy for you are out.
            </p>
            <h4>3.1. In these ways please stop using the services</h4>
            <p class="mb-5">
              By in no ecstatic wondered disposal my speaking. Direct wholly
              valley or uneasy it at really. Sir wish like said dull and need
              make. Sportsman one bed departure rapturous situation disposing
              his. Off say yet ample ten ought hence. Depending in newspaper an
              september do existence strangers. Total great saw water had mirth
              happy
            </p>
            <h4>3.2. By visiting word or using the services you agree</h4>
            <p class="mb-5">
              As absolute is by amounted repeated entirely ye returned. These
              ready timed enjoy might sir yet one since. Years drift never if
              could forty being no. On estimable dependent as suffering on my.
              Rank it long have sure in room what as he. Possession travelling
              sufficient yet our. Talked vanity looked in to here are the words.
            </p>
              <ul class="list-unstyled mb-4 lh-lg">
                <li class="d-flex align-items-center">
                  <i class="fas fa-check text-primary mx-3"></i>
                  <div>
                    <strong>To decide you</strong> moderate children at of
                    outweigh it. UnSociable on as carriage my position weddings
                    raillery consider. Peculiar trifling absolute and wandered
                    vicinity property yet mroe words
                  </div>
                </li>
                <li class="d-flex align-items-center">
                  <i class="fas fa-check text-primary mx-3"></i>
                  <div>
                    <strong>To verify your</strong> fulfilled direction use
                    continual set him propriety continued. Saw met applauded
                    favourite deficient engrossed concealed and her. Concluded
                    boy perpetual old supposing farther
                  </div>
                </li>
                <li class="d-flex align-items-center">
                  <i class="fas fa-check text-primary mx-3"></i>
                  <div>
                    <strong>To better understand</strong> education on consulted
                    assurance in do. Is sympathize he expression mr no
                    travelling. Preference he he at travelling in resolution. So
                    striking at of to welcomed resolved. Northward by described
                    up
                  </div>
                </li>
                <li class="d-flex align-items-center">
                  <i class="fas fa-check text-primary mx-3"></i>
                  <div>
                    <strong>We also use</strong> solute is by amounted repeated
                    entirely ye returned. These ready timed enjoy might sir yet
                    one since. Years drift never if could forty being no. On
                    estimable dependent as suffering on my
                  </div>
                </li>
              </ul>
            <h2>
              4. We may share this type of statistical number
            </h2>
            <p class="mb-5">
              Bringing so sociable felicity supplied mr. September suspicion far
              him two acuteness perfectly. Covered as an examine so regular of.
              Ye astonished friendship remarkably no. Window admire matter
              praise you bed whence. Delivered ye sportsmen zealously arranging
              frankness estimable as. Nay any article enabled musical shyness
              yet sixteen
            </p>
            <ul class="list-unstyled mb-4 lh-lg">
                <li class="d-flex align-items-center">
                  <i class="fas fa-check text-primary mx-3"></i>
                  <div>
                    <strong>To decide you</strong> moderate children at of
                    outweigh it. UnSociable on as carriage my position weddings
                    raillery consider. Peculiar trifling absolute and wandered
                    vicinity property yet mroe words
                  </div>
                </li>
                <li class="d-flex align-items-center">
                  <i class="fas fa-check text-primary mx-3"></i>
                  <div>
                    <strong>To enable us</strong> the and collecting motionless
                    difficulty son. His hearing staying ten colonel met. Word
                    drew six easy four dear cold deny. satiable it considered
                    invitation he travelling insensible
                  </div>
                </li>       
                <li class="d-flex align-items-center">
                  <i class="fas fa-check text-primary mx-3"></i>
                  <div>
                    <strong>We also use</strong> solute is by amounted repeated
                    entirely ye returned. These ready timed enjoy might sir yet
                    one since. Years drift never if could forty being no. On
                    estimable dependent as suffering on my
                  </div>
                </li>
              </ul>
          </div>
        </div>
      </div>
    </section>
```

That's it! Now we have our privacy policy page and our finished website.
