---
title: Responsive Design
tags: [CSS, HTML, Web Development, Responsive Design]
style: fill
color: warning
description: Responsive Web design is the approach that suggests that design and development should respond to the user's behavior and environment based on screen size, platform and orientation.
---

{% include elements/figure.html image="../assets/img/blogresponsive.jpg" caption="iOS" %}

Some real world responsive design examples

```html
html,
body {
  max-width: 1200px;
  margin: auto;
  font-family: "Space Mono", sans-serif;
  font-size: 18px;
  line-height: 1.4em;
  color: GhostWhite;
}

body {
  background-image: url("../img/space.jpg");
  height: 100%;
  background-attachment: fixed;
  background-size: cover;
}

.clearfix {
  clear: both;
}

/* Title and Description */

.page-title {
  text-align: center;
  margin: auto;
  line-height: 2em;
}

.logo {
  height: 80px;
  width: 80px;
  background-image: url("../img/spaceship.png");
  background-size: contain;
  background-repeat: no-repeat;
  display: inline-block;
  position: relative;
  top: 1em;
}

.page-title h1 {
  display: inline-block;
}

.main {
  text-align: center;
}

.page-description {
  font-size: 0.8rem;
  padding: 30px;
}

.learn-more {
  color: DarkOrange;
  text-decoration: none;
  display: block;
  margin: 25px 0 0 0;
  font-weight: bold;
}

/* Gallery */

.gallery {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 20px;
}

.gallery-item {
  margin: 20px;
}

.gallery-item .thumbnail {
  width: 240px;
  border: 2px solid GhostWhite;
  border-radius: 4px;
}

/* Footer Navigation */

nav {
  margin-top: 30px;
}

nav ul {
  display: block;
}

nav li {
  display: inline;
  margin: 0 20px 0 0;
  color: GhostWhite;
}

nav a {
  line-height: 60px;
  border: 1px solid GhostWhite;
  padding: 7px;
  border-radius: 4px;
  color: DarkOrange;
  text-decoration: none;
}

.contact-btn {
  cursor: pointer;
  margin: 20px 30px;
  text-align: center;
}

.contact-btn a:active {
  position: relative;
  bottom: 2px;
}

@media only screen and (min-width: 320px) and (max-width: 480px), (orientation: portrait) {
    /* ruleset for 320px - 480px */
  .gallery-item .thumbnail {
    width: 95%;
  }
}

@media only screen and (min-resolution: 150dpi) {
    /* CSS for high resolution screens */
  .logo {
    background-image: url("../img/spaceship@2x.png");
  }
}

@media only screen and (max-resolution: 150dpi) and (max-width: 480px) {
    /* CSS ruleset */
  .page-description {
    font-size: 20px;
  }
}

@media only screen and (min-width: 480px), (orientation: landscape) {
    /* CSS ruleset */
}

@media only screen and (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) {
    /* CSS ruleset */
  .page-title, .page-description {
    float: left;
    width: 20em;
  }

  .page-description {
    text-align: left;
  }
}

```

## Sizing Elements
```html
/* Universal Styles */

html {
  font-size: 16px;
}

body {
  background-color: white;
}

.image-container {
  overflow: hidden;

}

.image-container img {
  overflow: hidden;
  max-width: 100%;
  height: auto;
  display: block;
}

/* Banner Section */

#banner {
  height: 46rem;
  background-image: url('camel-background.png');
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

#banner h1 {
  font-size: 3.75rem;
  font-family: 'Roboto', sans-serif;
  font-weight: 300;
  color: white;
}

/* Blog Post */
p {
  min-width: 200px;
  min-height: 200px;
}
#blog {
  width: 86%;
  margin: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}

#blog .post {
  margin-bottom: 7.5%;
  margin-top: 12.5%;
  width: 52%;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: 'Merriweather', serif;
  font-weight: 300;
  font-size: 1rem;
  text-align: center;
  line-height: 1.8;
  color: #444444;
}

.post h2 {
  font-size: 1.875rem;
  
}

.post h3 {
  font-size: 1.125rem;
  color: #999999;
}

.post .opening-line {
  margin-top: 4.1875rem;
  margin-bottom: 1.5rem;
  color: black;
  font-weight: bold;
}

.post .image-container {
  width: 100%;
}

/* Blog Images */

.images {
  margin-bottom: 20%;
}

.images .image-container {
  display: inline-block;
  width: 50%;
}

/* Footer */

footer {
  padding: 4rem 0;
  border-top: 1px solid #999999;
  font-family: 'Roboto', sans-serif;
  font-size: 1.125rem;
  color: #999999;
  text-align: center;
}

```
