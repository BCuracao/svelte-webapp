<script>
  import video from "/src/lib/assets/home-video.mp4";
  import Selfie from "/src/lib/assets/portrait.png";
  import Background_img from "/src/lib/assets/skink_3_background.png";

  function showProfilePic() {}
</script>

<div class="background">
  <img class="skink" src={Background_img} alt="skink" />
  <div class="container content">
    <div class="video-container">
      <video src={video} autoplay loop muted />
    </div>
    <!-- 
    <div class="center-container">
      <div class="card card-1">
        <a
          style="text-decoration: none; color: rgb(88 199 250 / 60%);"
          href="https://www.linkedin.com/in/bastian-breindl-295571184/"
          target="_blank"
          rel="noopener noreferrer"
        >
          About <br /> me
          <img src={Selfie} alt="myself" class="card-image" />
        </a>
      </div>
    </div>

    <div class="center-container">
      <div class="card card-2">
        About <br /> me
        <img src={Selfie} alt="myself" class="card-image" />
      </div>
    </div>

    -->

    <div class="company">
      <div class="company__container">
        <p class="company__container__text">Hello</p>

        <ul class="company__container__list">
          <li class="company__container__list__item">world !</li>
          <li class="company__container__list__item">customer !</li>
          <li class="company__container__list__item">friend !</li>
          <li class="company__container__list__item">colleague !</li>
        </ul>
      </div>
    </div>
    <div class="company-name">
      <div class="company__container">
        <p class="company__container__text">Welcome to Browse ;T</p>
      </div>
    </div>
    <!--
    <label>
      <input type="checkbox" />
      <span class="menu">
        <span class="hamburger" />
      </span>
      <ul>
        <li>
          <a href="#">Home</a>
        </li>
        <li>
          <a href="#">About</a>
        </li>
        <li>
          <a href="#">Work</a>
        </li>
      </ul>
    </label>
     -->

    <!-- 
    <div class="arrow-container">
      <div class="object">
        <img src={Selfie} alt="" class="object__img" />
        <div class="object__intro">
          <p class="object__intro-text">Click to find me</p>
        </div>
      </div>

      <div class="arrow">
        <div class="arrow__body" />
      </div>
    </div>
    -->
    <div class="center-container-dottedline">
      <svg
        xmlns:xlink="http://www.w3.org/1999/xlink"
        width="340"
        height="333"
        viewBox="0 0 340 333"
        left:
      >
        <defs>
          <path
            id="path1"
            d="M66.039,203.545c50,0-21-57,18-67s49-4,65,8s30,41,53,27s66,4,58,32s-5,44,18,57s22,46,0"
          />
          <mask id="mask1"><use class="mask" xlink:href="#path1" /></mask>
        </defs>
        <use class="paths" xlink:href="#path1" mask="url(#mask1)" />
      </svg>
    </div>

    <div class="center-container-object">
      <div class="object delayed-show">
        <img src={Selfie} alt="" class="object__img" />
        <div class="object__intro">
          <p class="object__intro-text">.Me</p>
        </div>
      </div>
    </div>
  </div>
</div>

<style>
  .background {
    position: absolute;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    background-color: rgba(56, 56, 56, 0.349);
    background-clip: padding-box;
    z-index: -25;
  }

  .container.content {
    position: absolute;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    border: solid 0px rgb(35, 40, 50);
    overflow: hidden;
    border-radius: 0% 0% 0% 0%;
  }

  .skink {
    position: absolute;
    bottom: -100px;
    left: -155px;
    z-index: -5;
    opacity: 60%;
    max-width: 50%;
    max-height: 50%;
    transform: rotate(0deg);
  }

  /* BACKGROUND VIDEO */
  video {
    width: 100%;
    height: 100%;
    position: absolute;
    padding: 0;
    margin: 0;
    left: 0px;
    top: 0px;
    z-index: -1000;
    overflow: hidden;
    object-fit: cover;
  }

  /* THE CARD */
  @property --rotate {
    syntax: "<angle>";
    initial-value: 132deg;
    inherits: false;
  }

  :root {
    --card-height: 20vh;
    --card-width: calc(var(--card-height) / 1.5);
  }

  body {
    min-height: 100vh;
    background: #212534;
    display: flex;
    align-items: center;
    flex-direction: column;
    padding-top: 2rem;
    padding-bottom: 2rem;
    box-sizing: border-box;
    overflow: hidden;
  }

  .card {
    background: #191c29;
    opacity: 100%;
    width: var(--card-width);
    height: var(--card-height);
    padding: 3px;
    position: absolute; /* Use absolute positioning */
    justify-content: center;
    align-items: center;
    text-align: center;
    border-radius: 6px;
    display: flex;
    font-size: 1.25em;
    color: rgb(88 199 250 / 60%);
    cursor: pointer;
    font-family: monospace;
    letter-spacing: 0.35rem;
  }

  .card.card-1 {
    top: 45%; /* Adjust the top position for card-1 */
    left: 33%; /* Adjust the left position for card-1 */
  }

  .card.card-2 {
    top: 65%; /* Adjust the top position for card-2 */
    left: 58%; /* Adjust the left position for card-2 */
  }

  .center-container {
    display: flex;
    justify-content: center;
    align-items: center;
    /* Add margin or padding as needed to separate the cards vertically */
    margin-bottom: 20px; /* Example: Adds some spacing between cards */
  }

  .card:hover {
    color: rgb(88 199 250 / 100%);
    transition: color 1s;
    opacity: 80%;
  }

  /* Add a class to style the image when it's inside the .card */
  .card-image {
    width: 100%; /* Set the image width to 100% of the .card */
    height: 100%; /* Set the image height to 100% of the .card */
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0; /* Initially hide the image */
    transition: opacity 0.5s; /* Add a transition effect for opacity */
  }

  .card:hover .card-image {
    opacity: 1; /* Show the image on hover */
  }

  .card:hover:before,
  .card:hover:after {
    animation: none;
    opacity: 0;
  }

  .card::before {
    content: "";
    width: 104%;
    height: 102%;
    border-radius: 8px;
    background-image: linear-gradient(
      var(--rotate),
      #5ddcff,
      #3c67e3 43%,
      #4e00c2
    );
    position: absolute;
    z-index: -1;
    top: -1%;
    left: -2%;
    animation: spin 2.5s linear infinite;
  }

  .card::after {
    position: absolute;
    content: "";
    top: calc(var(--card-height) / 6);
    left: 0;
    right: 0;
    z-index: -1;
    height: 100%;
    width: 100%;
    margin: 0 auto;
    transform: scale(0.8);
    filter: blur(calc(var(--card-height) / 6));
    background-image: linear-gradient(
      var(--rotate),
      #5ddcff,
      #3c67e3 43%,
      #4e00c2
    );
    opacity: 1;
    transition: opacity 0.5s;
    animation: spin 2.5s linear infinite;
  }

  @keyframes spin {
    0% {
      --rotate: 0deg;
    }
    100% {
      --rotate: 360deg;
    }
  }

  /*TEXT ANIMATION*/
  body {
    width: 100%;
    height: 100%;
    position: fixed;
    background-color: #34495e;
  }
  .company {
    position: absolute;
    top: 90%;
    left: 20%;
    transform: translate(-50%, -50%);
    height: 160px;
    overflow: hidden;
    font-family: "Lato", sans-serif;
    font-size: 35px;
    line-height: 40px;
    color: #ecf0f1;
  }

  .company-name {
    position: absolute;
    top: 95%;
    left: 26.1%;
    transform: translate(-50%, -50%);
    height: 120px;
    overflow: hidden;
    font-family: "Lato", sans-serif;
    font-size: 35px;
    line-height: 40px;
    color: #ecf0f1;
  }
  .company__container {
    font-weight: 600;
    overflow: hidden;
    height: 40px;
    padding: 0 40px;
  }
  .company__container:before {
    content: "[";
    left: 0;
  }
  .company__container:after {
    content: "]";
    position: absolute;
    right: 0;
  }
  .company__container:after,
  .company__container:before {
    position: absolute;
    top: 0;
    color: #16a085;
    font-size: 42px;
    line-height: 40px;
    -webkit-animation-name: opacity;
    -webkit-animation-duration: 2s;
    -webkit-animation-iteration-count: infinite;
    animation-name: opacity;
    animation-duration: 2s;
    animation-iteration-count: infinite;
  }
  .company__container__text {
    letter-spacing: 0x;
    display: inline;
    float: left;
    margin: 0;
  }
  .company__container__list {
    margin-top: 0;
    padding-left: 110px;
    text-align: left;
    list-style: none;
    -webkit-animation-name: change;
    -webkit-animation-duration: 10s;
    -webkit-animation-iteration-count: infinite;
    animation-name: change;
    animation-duration: 10s;
    animation-iteration-count: infinite;
  }
  .company__container__list__item {
    line-height: 40px;
    margin: 0;
  }
  @-webkit-keyframes opacity {
    0%,
    100% {
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
  }
  @-webkit-keyframes change {
    0%,
    12.66%,
    100% {
      transform: translate3d(0, 0, 0);
    }
    16.66%,
    29.32% {
      transform: translate3d(0, -25%, 0);
    }
    33.32%,
    45.98% {
      transform: translate3d(0, -50%, 0);
    }
    49.98%,
    62.64% {
      transform: translate3d(0, -75%, 0);
    }
    66.64%,
    79.3% {
      transform: translate3d(0, -50%, 0);
    }
    83.3%,
    95.96% {
      transform: translate3d(0, -25%, 0);
    }
  }
  @-o-keyframes opacity {
    0%,
    100% {
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
  }
  @-o-keyframes change {
    0%,
    12.66%,
    100% {
      transform: translate3d(0, 0, 0);
    }
    16.66%,
    29.32% {
      transform: translate3d(0, -25%, 0);
    }
    33.32%,
    45.98% {
      transform: translate3d(0, -50%, 0);
    }
    49.98%,
    62.64% {
      transform: translate3d(0, -75%, 0);
    }
    66.64%,
    79.3% {
      transform: translate3d(0, -50%, 0);
    }
    83.3%,
    95.96% {
      transform: translate3d(0, -25%, 0);
    }
  }
  @-moz-keyframes opacity {
    0%,
    100% {
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
  }
  @-moz-keyframes change {
    0%,
    12.66%,
    100% {
      transform: translate3d(0, 0, 0);
    }
    16.66%,
    29.32% {
      transform: translate3d(0, -25%, 0);
    }
    33.32%,
    45.98% {
      transform: translate3d(0, -50%, 0);
    }
    49.98%,
    62.64% {
      transform: translate3d(0, -75%, 0);
    }
    66.64%,
    79.3% {
      transform: translate3d(0, -50%, 0);
    }
    83.3%,
    95.96% {
      transform: translate3d(0, -25%, 0);
    }
  }
  @keyframes opacity {
    0%,
    100% {
      opacity: 0;
    }
    50% {
      opacity: 1;
    }
  }
  @keyframes change {
    0%,
    12.66%,
    100% {
      transform: translate3d(0, 0, 0);
    }
    16.66%,
    29.32% {
      transform: translate3d(0, -25%, 0);
    }
    33.32%,
    45.98% {
      transform: translate3d(0, -50%, 0);
    }
    49.98%,
    62.64% {
      transform: translate3d(0, -75%, 0);
    }
    66.64%,
    79.3% {
      transform: translate3d(0, -50%, 0);
    }
    83.3%,
    95.96% {
      transform: translate3d(0, -25%, 0);
    }
  }

  /* INFO BOX */
  /* KEYFRAMES */
  @keyframes spin {
    from {
      transform: rotate(0);
    }
    to {
      transform: rotate(359deg);
    }
  }
  @keyframes spin3D {
    from {
      transform: rotate3d(0.5, 0.5, 0.5, 360deg);
    }
    to {
      transform: rotate3d(0deg);
    }
  }
  @keyframes configure-clockwise {
    0% {
      transform: rotate(0);
    }
    25% {
      transform: rotate(90deg);
    }
    50% {
      transform: rotate(180deg);
    }
    75% {
      transform: rotate(270deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
  @keyframes configure-xclockwise {
    0% {
      transform: rotate(45deg);
    }
    25% {
      transform: rotate(-45deg);
    }
    50% {
      transform: rotate(-135deg);
    }
    75% {
      transform: rotate(-225deg);
    }
    100% {
      transform: rotate(-315deg);
    }
  }
  @keyframes pulse {
    from {
      opacity: 1;
      transform: scale(1);
    }
    to {
      opacity: 0.25;
      transform: scale(0.75);
    }
  }

  /* MENU NAV TEST */

  @import url("https://fonts.googleapis.com/css?family=Cutive+Mono");
  *,
  *:before,
  *:after {
    box-sizing: border-box;
  }

  label .menu {
    position: absolute;
    right: 0px;
    top: 0px;
    z-index: 100;
    width: 100px;
    height: 100px;
    background: #fff;
    border-radius: 50% 50% 50% 50%;
    transition: 0.5s ease-in-out;
    box-shadow: 0 0 0 0 #fff, 0 0 0 0 #fff;
    cursor: pointer;
    opacity: 40%;
  }
  label .hamburger {
    position: absolute;
    top: 50px;
    left: 35px;
    width: 30px;
    height: 2px;
    background: #000;
    display: block;
    transform-origin: center;
    transition: 0.5s ease-in-out;
  }
  label .hamburger:after,
  label .hamburger:before {
    transition: 0.5s ease-in-out;
    content: "";
    position: absolute;
    display: block;
    width: 100%;
    height: 100%;
    background: #000;
  }
  label .hamburger:before {
    top: -10px;
  }
  label .hamburger:after {
    bottom: -10px;
  }
  label input {
    display: none;
  }
  label input:checked + .menu {
    box-shadow: 0 0 0 10vw #fff, 0 0 0 100vh #fff;
    border-radius: 0;
  }
  label input:checked + .menu .hamburger {
    transform: rotate(45deg);
  }
  label input:checked + .menu .hamburger:after {
    transform: rotate(90deg);
    bottom: 0;
  }
  label input:checked + .menu .hamburger:before {
    transform: rotate(90deg);
    top: 0;
  }
  label input:checked + .menu + ul {
    opacity: 1;
  }
  label ul {
    z-index: 200;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    opacity: 0;
    transition: 0.25s 0s ease-in-out;
  }
  label a {
    margin-bottom: 1em;
    display: block;
    color: #000;
    text-decoration: none;
  }
  h1 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 80%;
    text-align: center;
  }

  /* PROFILE */

  .object {
    display: none;
    position: relative;
    width: 100px;
    height: 100px;
    z-index: 1;
    border-radius: 50%;
    border-width: 20px;
    border-color: black;
    border: 3px solid #87fce4;
    opacity: 70%;
  }
  .object:hover {
    opacity: 100%;
  }
  .object__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border: 5px solid var(--highlight-color);
    border-radius: 50%;
    border-width: 20px;
    border-color: black;
  }

  .object__intro {
    position: absolute;
    top: 50%;
    left: 100%;
    transform: translateY(-50%);
    width: 300px;
    padding-left: 10px;
    color: var(--highlight-color);
  }

  .object__intro-text {
    line-height: 1.5;
    font-size: 20px;
    color: #87fce4;
  }

  .center-container-object {
    display: block;
    justify-content: center;
    align-items: center;
    /* Add margin or padding as needed to separate the cards vertically */
    margin-top: -100px; /* Example: Adds some spacing between cards */
    margin-left: 1000px;
  }

  @keyframes showObject {
    to {
      display: block; /* Show the object when animation completes */
    }
  }

  .object.delayed-show {
    animation: showObject 2s; /* Apply the animation with a 5-second delay */
  }

  /* DOTTED LINE */

  .paths {
    fill: none;
    stroke: #87fce4;
    stroke-dasharray: 5;
    stroke-width: 5;
    stroke-linejoin: round;
    opacity: 70%;
  }

  .mask {
    fill: none;
    stroke: white;
    stroke-width: 10;
    stroke-dasharray: 1000;
    stroke-dashoffset: 1000;
    animation: dash 5s linear alternate forwards;
  }

  /* does not work in IE, need JS to animate there */
  @keyframes dash {
    from {
      stroke-dashoffset: 1000;
    }
    to {
      stroke-dashoffset: 0;
    }
  }

  .center-container-dottedline {
    display: flex;
    justify-content: center;
    align-items: center;
    /* Add margin or padding as needed to separate the cards vertically */
    margin-top: 200px; /* Example: Adds some spacing between cards */
    margin-left: 700px;
  }
</style>
