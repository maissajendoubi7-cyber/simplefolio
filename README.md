# Simplefolio ⚡️ [![GitHub](https://img.shields.io/github/license/cobiwave/simplefolio?color=blue)](https://github.com/cobiwave/simplefolio/blob/master/LICENSE.md) ![GitHub stars](https://img.shields.io/github/stars/cobiwave/simplefolio) ![GitHub forks](https://img.shields.io/github/forks/cobiwave/simplefolio)

## A minimal portfolio template for Developers!

<h2 align="center">
  <img src="https://github.com/cobiwave/gatsby-simplefolio/blob/master/examples/example.gif" alt="Simplefolio" width="600px" />
  <br>
</h2>

## Features

⚡️ Modern UI Design + Reveal Animations\
⚡️ One Page Layout\
⚡️ Styled with Bootstrap v4.3 + Custom SCSS\
⚡️ Fully Responsive\
⚡️ Valid HTML5 & CSS3\
⚡️ Optimized with Parcel\
⚡️ Well organized documentation

To view the demo: **[click here](https://the-simplefolio.netlify.app/)**

---

## Why do you need a portfolio? ☝️

- Professional way to showcase your work
- Increases your visibility and online presence
- Shows you’re more than just a resume

## Getting Started 🚀

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites 📋

You'll need [Git](https://git-scm.com) and [Node.js](https://nodejs.org/en/download/) (which comes with [NPM](http://npmjs.com)) installed on your computer.

```
node@v16.4.2 or higher
npm@7.18.1 or higher
git@2.30.1 or higher
```

Also, you can use [Yarn](https://yarnpkg.com/) instead of NPM ☝️

```
yarn@v1.22.10 or higher
```

---

## How To Use 🔧

From your command line, first clone Simplefolio:

```bash
# Clone the repository
$ git clone https://github.com/cobiwave/simplefolio

# Move into the repository
$ cd simplefolio

# Remove the current origin repository
$ git remote remove origin
```

After that, you can install the dependencies either using NPM or Yarn.

Using NPM: Simply run the below commands.

```bash
# 2022 Update - Fix Dependencies
$ npm audit fix
$ npm i @parcel/transformer-sass

# Install dependencies
$ npm install

# Start the development server
$ npm start
```

Using Yarn: Be aware of that you'll need to delete the `package-lock.json` file before executing the below commands.

```bash
# Install dependencies
$ yarn

# Start the development server
$ yarn start
```

**NOTE**:
If your run into issues installing the dependencies with NPM, use this below command:

```bash
# Install dependencies with all permissions
$ sudo npm install --unsafe-perm=true --allow-root
```

Once your server has started, go to this url `http://localhost:1234/` to see the portfolio locally. It should look like the below screenshot.

<h2 align="center">
  <img src="https://github.com/cobiwave/gatsby-simplefolio/blob/master/examples/example.png" alt="Simplefolio" width="100%">
</h2>

---

## Template Instructions:

### Step 1 - STRUCTURE

Go to `/src/index.html` and put your information, there are 5 sections:

### (1) Hero Section

- On `.hero-title`, put your custom portfolio title.
- On `.hero-cta`, put your custom button label.
html
<header id="header">
  <div class="logo"><span class="icon fa-gem"></span></div>
  <div class="content">
    <div class="inner">
      <h1>Jane Doe</h1>
      <p>Web Developer | Designer | Creator</p>
    </div>
  </div>
</header>
```

### (2) About Section

- On `<img>` tag, fill the `src` property with your profile picture path, your picture must be located inside `/src/assets/` folder.
- On `<p>` tag with class name `.about-wrapper__info-text`, include information about you, I recommend to put 2 paragraphs in order to work well and a maximum of 3 paragraphs.
- On last `<a>` tag, include your CV (.pdf) path on `href` property, your resume CV must be located inside `/src/assets/` folder.

```html
<!-- **** About Section **** -->
<section id="about">
  <div class="container">
    <h2 class="section-title load-hidden">About me</h2>
    <div class="row about-wrapper">
      <div class="col-md-6 col-sm-12">
        <div class="about-wrapper__image load-hidden">
          <img
            alt="Profile Image"
            class="img-fluid rounded shadow-lg"
            height="auto"
            width="300px"
            src="assets/profile.jpg"
            alt="Profile Image"
          />
        </div>
      </div>
      <div class="col-md-6 col-sm-12">
        <div class="about-wrapper__info load-hidden">
          <p class="about-wrapper__info-text">
            This is where you can describe about yourself. The more you describe
            about yourself, the more chances you can!
          </p>
          <p class="about-wrapper__info-text">
            Extra Information about you! like hobbies and your goals.
          </p>
          <span class="d-flex mt-3">
            <a
              rel="noreferrer"
              target="_blank"
              class="cta-btn cta-btn--resume"
              href="assets/resume.pdf"
            >
              View Resume
            </a>
          </span>
        </div>
      </div>
    </div>
  </div>
</section>
<!-- /END About Section -->
```

### (3) Projects Section

- Each project lives inside a `row`.
- On `<h3>` tag with class name `.project-wrapper__text-title`, include your project title.
- On `<p>` tag with `loremp ipsum` text, include your project description.
- On first `<a>` tag, put your project url on `href` property.
- On second `<a>` tag, put your project repository url on `href` property.

---

- Inside `<div>` tag with class name `.project-wrapper__image`, put your project image url on the `src` of the `<img>` and put again your project url in the `href` property of the `<a>` tag.
- Recommended size for project image (1366 x 767), your project image must be located inside `/src/assets/` folder.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Maïssa Jendoubi - Portfolio</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f7f7f7;
      margin: 0;
      padding: 0;
    }
    header {
      background: #1e1e2f;
      color: white;
      text-align: center;
      padding: 2rem 0;
    }
    section {
      max-width: 800px;
      margin: 2rem auto;
      background: white;
      padding: 1.5rem;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h2 { color: #333; }
  </style>
</head>
<body>
  <header>
    <h1>👩‍💻 Maïssa Jendoubi</h1>
    <p>Développeuse web | Passionnée de technologie</p>
  </header>

  <section>
    <h2>À propos de moi</h2>
    <p>Je suis développeuse web en formation, j’aime créer des sites modernes et utiles.</p>
  </section>

  <section>
    <h2>Mes projets</h2>
    <ul>
      <li>🌐 <strong>Nsi7a</strong> — Site de conseils et échanges entre utilisateurs</li>
      <li>☀️ Application météo en JavaScript</li>
      <li>💻 Mini blog avec HTML & CSS</li>
    </ul>
  </section>

  <section>
    <h2>Contact</h2>
    <p>Email : <a href="mailto:maissa@example.com">maissa@example.com</a></p>
    <p>GitHub : <a href="https://github.com/tonnom">github.com/tonnom</a></p>
  </section>
</body>
</html>


### (4) Contact Section

- On `<p>` tag with class name `.contact-wrapper__text`, include some custom call-to-action message.
- On `<a>` tag, put your email address on `href` property.

```html
<!-- **** Contact Section **** -->
<section id="contact">
  <div class="container">
    <h2 class="section-title">Contact</h2>
    <div class="contact-wrapper load-hidden">
      <p class="contact-wrapper__text">[Put your call to action here]</p>
      <a
        rel="noreferrer"
        target="_blank"
        class="cta-btn cta-btn--resume"
        href="mailto:example@email.com"
        >Call to Action</a
      >
    </div>
  </div>
</section>
<!-- /END Contact Section -->
```

### (5) Footer Section

- Put your Social Media URL on each `href` attribute of the `<a>` tags.
- If you an additional Social Media account different than Twitter, Linkedin or GitHub, then go to [Font Awesome Icons](https://fontawesome.com/v4.7.0/icons/) and search for the icon's class name you are looking.
- You can delete or add as many `<a>` tags your want.

```html
<footer class="footer navbar-static-bottom">
  ...
  <div class="social-links">
    <a href="#!" target="_blank">
      <i class="fa fa-twitter fa-inverse"></i>
    </a>
    <a href="#!" target="_blank">
      <i class="fa fa-linkedin fa-inverse"></i>
    </a>
    <a href="#!" target="_blank">
      <i class="fa fa-github fa-inverse"></i>
    </a>
  </div>
  ...
</footer>
```

### Step 2 - STYLES

Change the color theme of the website - (choose 2 colors to create a gradient)

Go to `/src/sass/abstracts/_variables.scss` and only change the values for this variables `$main-color` and `$secondary-color` with your prefered HEX color.
If you want to get some gradients inspiration I highly recommend you to check this website [UI Gradient](https://uigradients.com/#BrightVault)

```scss
// Default values
$main-color: #02aab0;
$secondary-color: #00cdac;
```

---

## Deployment 📦

Once you finish your setup. You need to put your website online!

I highly recommend to use [Netlify](https://netlify.com) because it is super easy.

## Others versions 👥

[Gatsby Simplefolio](https://github.com/cobiwave/gatsby-simplefolio) by [Jacobo Martinez](https://github.com/cobiwave)\
[Ember.js Simplefolio](https://github.com/sernadesigns/simplefolio-ember) by [Michael Serna](https://github.com/sernadesigns)

## Technologies used 🛠️

- [Parcel](https://parceljs.org/) - Bundler
- [Bootstrap 4](https://getbootstrap.com/docs/4.3/getting-started/introduction/) - Frontend component library
- [Sass](https://sass-lang.com/documentation) - CSS extension language
- [ScrollReveal.js](https://scrollrevealjs.org/) - JavaScript library
- [Tilt.js](https://gijsroge.github.io/tilt.js/) - JavaScript tiny parallax library

## Authors

- **Jacobo Martinez** - [https://github.com/cobiwave](https://github.com/cobiwave)

## Status

[![Netlify Status](https://api.netlify.com/api/v1/badges/3a029bfd-575c-41e5-8249-c864d482c2e5/deploy-status)](https://app.netlify.com/sites/the-simplefolio/deploys)

## License 📄

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments 🎁

I was motivated to create this project because I wanted to contribute on something useful for the dev community, thanks to [ZTM Community](https://github.com/zero-to-mastery) and [Andrei](https://github.com/aneagoie)
