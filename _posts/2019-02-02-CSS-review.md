---
title: CSS Review
tags: [Web Development, CSS]
style: fill
color: info
description: some real-world examples for you implement your HTML codes
---

Some real world CSS examples

```html
body {
  /* Old browsers */
  background: #141E30;
  /* Chrome 10-25, Safari 5.1-6 */
  background: -webkit-linear-gradient(-45deg, #35577D, #141E30);
  /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  background: linear-gradient(-45deg, #35577D, #141E30);
  margin: 0;
  padding: 0;
}

h1 {
  color: #FFF;
  font-size: 2em;
  padding-top: 100px;
  width: 100%;
  font-family: "Georgia";
  text-align: center;
}

h2 {
  border-bottom: 1px solid rgba(255, 255, 255, 0.5);
  color: rgba(255, 255, 255, 0.5);
  font-weight: 100;
  font-size: 22px;
  line-height: 24px;
  padding-bottom: 30px;
  text-align: left;
  width: 70%;
  font-family: "Georgia";
}

p {
  color: AliceBlue;
  line-height: 1.3em;
  text-align: left;
  width: 100%;
  font-size: 18px;
  font-weight: bold;
  font-family: "Helvetica";
}

.byline {
  font-family: Helvetica;
  color: rgba(255, 255, 255, 0.5);
  float: left;
  font-size: 14px;
  padding-left: 10px;
  text-transform: uppercase;
}

.caption {
  display: block;
  font-family: 'Playfair Display', serif;
  font-size: 14px;
  font-style: italic;
  line-height: 14px;
  margin-left: 20px;
  padding: 10px;
  position: relative;
  top: 80%;
  width: 60%;
  color: black;
  background-color: white;
  opacity: 0.75;
}

.content {
  padding: 40px;
}

.image {
  background-image: url("https://s3.amazonaws.com/codecademy-content/courses/freelance-1/unit-2/soccer.jpeg");
  background-size: cover;
  background-position: center;
  height: 300px;
}

.writer-img {
  -webkit-box-shadow: 5px 0px 5px 0px rgba(0, 0, 50, 0.97);
  -moz-box-shadow: 5px 0px 5px 0px rgba(0, 0, 50, 0.97);
  box-shadow: 5px 0px 5px 0px rgba(0, 0, 50, 0.97);
  float: left;
  width: 50px;
}


```

## 

```html
@font-face {
  font-family: WorkSans;
  src: url("https://s3.amazonaws.com/codecademy-content/courses/learn-css-grid/project-ii/Resources/Work_Sans/WorkSans-Regular.ttf");
}
@font-face {
  font-family: Poppins;
  src: url("https://s3.amazonaws.com/codecademy-content/courses/learn-css-grid/project-ii/Resources/Poppins/Poppins-Regular.ttf");
}

html {
  height: 100%;
}

body {
  height: 100%;
  margin: 0;
  background-image: linear-gradient(359deg, #3023ae, #eb7f7b);
  background-repeat: no-repeat;
  background-attachment: fixed;
}

.navbar {
  display: grid;
  grid-template-columns: 10px 1fr 3fr 1fr;
  position: absolute;
  width: 100%;
  height: 60px;
  background-color: rgba(120,70,154, 0.2);
  text-align: center;
  top: 0;
  left: 0;
  justify-content: space-around;
}

.navbar h1 {
  grid-column: 3 / 4;
  font-family: Poppins;
  color: #ffffff;
  margin: 0;
  align-self: center;
}

.container {
  width: 1000px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-column-gap: 20px;
  grid-auto-rows: 100px;
}

.search-bar {
  grid-column: 2 / 3;
  width: 100%;
  height: 40px;
  background-color: rgba(255,255,255, 0.35);
  top: 8px;
  position: absolute;
}

input {
  display: inline-block;
  border: none;
  background: transparent;
  font-size: 14px;
}

.search-bar input {
  float: left;
  height: 18px;
  margin-top: 9px;
  margin-left: 7px; 
}

.card-column input {
  height: 18px;
  margin-left: 15px;    
}

.search-icon {
  float: left;  
  margin-top: 9px;
  margin-left: 7px;
}

.card-column {
  background-color: #ffffff;
  grid-gap: 10px;
  min-height: 700px;
  display: grid;
  grid-template-rows: 20px repeat(5, 100px);
  align-content: space-between;
}

.card-column h2 {
  padding: 0;
  margin: 0 auto;
  font-family: WorkSans;
  font-size: 16px;
  font-weight: 600;
  letter-spacing: 0.2px;
  text-align: left;
  color: #2f2f2f;
  display: inline-block;
}

.taskgroup-heading {
  margin-left: 15px;
  margin-top: 7px;
}

.site-body {
  position: absolute;
  top: 100px;
  margin-left: 50px;
}

.card {
  margin-right: 15px;
  margin-left: 15px;
  background-color: rgba(216, 216, 216, 0.21);
  border: solid 1px rgba(151,151,151,0.21);
  position: relative;
}

.rectangle {
  width: 57px;
  height: 6px;
  position: relative;
  display: inline-block;
  margin-left: 7px;
}

.list-icon {
  display: inline-block;
  margin-left: 7px;
  margin-bottom: 5px;
  position: absolute;
  bottom: 0;
}

.task-description {
  margin-left: 7px;
  margin-top: 0;
  font-family: WorkSans;
  font-size: 14px;
  letter-spacing: 0.2px;
  text-align: left;
  color: #2f2f2f;
}

.ellipsis-icon {
  display: inline-block;
  float: right;
  margin-right: 15px;
}

.task-date {
  display: inline-block;
  font-family: WorkSans;
  font-size: 10px;
  letter-spacing: 0.1px;
  text-align: left;
  color: #9b9b9b;
  position: absolute;
  bottom: 0;
  margin-bottom: 5px;
  left: 25px;
}

.yellow {
  background-color: #fdcb1e;
}

.orange {
  background-color: #ff7700;
}

.green {
  background-color: #50e3c2;
}

.blue {
  background-color: #3343e5;
}

.add-card {
  background-color: rgba(216, 216, 216, 0.21);
  border: solid 1px rgba(151,151,151,0.21);
  color: #2f2f2f;
}

.completed-projects {
  grid-template-rows: 20px;
  grid-auto-rows: 100px;
}


```