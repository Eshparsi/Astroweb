<script>
    let slideIndex = 1;
  
    function plusSlides(n) {
      showSlides(slideIndex += n);
    }
  
    function currentSlide(n) {
      showSlides(slideIndex = n);
    }
  
    function showSlides(n) {
      let i;
      let slides = document.getElementsByClassName("mySlides");
      let dots = document.getElementsByClassName("dot");
      if (n > slides.length) {slideIndex = 1}
      if (n < 1) {slideIndex = slides.length}
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      for (i = 0; i < dots.length; i++) {
        dots[i].className = dots[i].className.replace(" active", "");
      }
      slides[slideIndex-1].style.display = "block";
      dots[slideIndex-1].className += " active";
    }
</script>
  
<style>
    * {
        box-sizing: border-box;
    }
    body {font-family: Verdana, sans-serif; margin:0; background-color: black;}
    .mySlides {display: none}
    img {vertical-align: middle;}
  
    /* Slideshow container */
    .slideshow-container {
      max-width: 1000px;
      position: relative;
      margin: auto;
    }
  
    /* Next & previous buttons */
    .prev, .next {
      cursor: pointer;
      position: absolute;
      top: 50%;
      width: auto;
      padding: 16px;
      margin-top: -22px;
      color: white;
      font-weight: bold;
      font-size: 18px;
      transition: 0.6s ease;
      border-radius: 0 3px 3px 0;
      user-select: none;
    }
  
    /* Position the "next button" to the right */
    .next {
      right: 0;
      border-radius: 3px 0 0 3px;
    }
  
    /* On hover, add a black background color with a little bit see-through */
    .prev:hover, .next:hover {
      background-color: rgba(92, 87, 87, 0.8);
    }
  
    /* Caption text */
    .text {
      color: #f2f2f2;
      font-size: 15px;
      padding: 8px 12px;
      position: absolute;
      bottom: 8px;
      width: 100%;
      text-align: center;
    }
  
    /* Number text (1/3 etc) */
    .numbertext {
      color: #f2f2f2;
      font-size: 12px;
      padding: 8px 12px;
      position: absolute;
      top: 0;
    }
  
    /* The dots/bullets/indicators */
    .dot {
      cursor: pointer;
      height: 15px;
      width: 15px;
      margin: 0 2px;
      background-color: #bbb;
      border-radius: 50%;
      display: inline-block;
      transition: background-color 0.6s ease;
    }
  
    .active, .dot:hover {
      background-color: #717171;
    }
  
    /* Fading animation */
    .fade {
      animation-name: fade;
      animation-duration: 1.5s;
    }
  
    #navbar a{
        color: white;
        text-decoration: none;
        font-size: 20px;
        padding: 10px;
        margin: 10px;
        border-radius: 5px;
        transition: 0.3s;
        display : flex;
        justify-content: flex-end;
        cursor: pointer;
    }
    nav ul{
        list-style: none;
        background: #79548c;
        overflow: hidden;
        color: white;
        padding: 0;
        text-align: right;
        margin: 0;
        transition: 1s;
    }
  
  
    nav.black ul{
        background: #0D0D0D;
    }
  
    nav ul li{
        display: inline-block;
        padding: 20px;
    }
  
    nav ul li a{
        text-decoration: none;
        color: white;
        font-size: 18px;
        cursor: pointer;
    }
  
    nav ul li a:hover {
        border-bottom: 2px solid #79548c;
    }
  
    nav ul li a.active {
        border-bottom: 2px solid #79548c;
    }
  
    .about-me {
        align-items: center;
    }
  
    #about-me h2 {
        font-size: 40px;
        margin-top: 10px;
        color: #79548c;
        padding: 15px;
        padding-left: 0;
    }
  
    #about-me p {
        font-size: 15px;
        color: #ddcfcf;
        margin-top: -1cm;
        padding-left: 220px;
        padding-right: 220px;
    }
  
    #about-me span {
        border-bottom: 1px solid #79548c;
    }
    .logo{
      position: relative;
      float: left;
      cursor: pointer;
    }
    footer {
      text-align: center;
      padding: 3px;
      background-color: #79548c;
      color: white;
    }
  
    @keyframes fade {
      from {opacity: .4} 
      to {opacity: 1}
    }
  
    /* On smaller screens, decrease text size */
    @media only screen and (max-width: 300px) {
      .prev, .next,.text {font-size: 11px}
    }
  </style>
  
  <!-- HTML content -->
  
  <svelte:head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>About Us</title>
    <link rel="stylesheet" href="about.css">
    <link rel="icon" type="image/x-icon" href="photos/logo.jpg">
    <link rel="icon" type="image/jpg" sizes="32x32" href="photos/logo.jpg">
    <link rel="icon" type="image/jpg" sizes="16x16" href="photos/logo.jpg">
  </svelte:head>
  
  <div>
    <header>
        <nav>
          <div class="logo"><a href="" target="_blank"><img src="photos/logo.jpg" width="50" height="61"></a></div>
          <div class="menu">
                <ul>
                    <li><a href="main.html">Chat</a></li>
                    <li><a href="about.html">About us</a></li>
                    <li><a href="faq.html">FAQs</a></li>
                    <li><a href="news.html">News</a></li>
                </ul>
            </div>
        </nav>
    </header>
  <!-- ... (Previous code remains unchanged) -->

  <div class="slideshow-container">
    <div class="mySlides fade">
      <div class="numbertext">1 / 3</div>
      <img src="photos/s1.jpg" style="width:100%">
      <div class="text">Explore the Cosmos with AstroChat</div>
    </div>

    <div class="mySlides fade">
      <div class="numbertext">2 / 3</div>
      <img src="photos/s2.jpg" style="width:100%">
      <div class="text">Unveiling the Beauty and Mystery of Space</div>
    </div>

    <div class="mySlides fade">
      <div class="numbertext">3 / 3</div>
      <img src="photos/s5.jpg" style="width:100%">
      <div class="text">Get Started</div>
    </div>

    <a class="prev" onclick="plusSlides(-1)">+</a>
    <a class="next" onclick="plusSlides(1)">-</a>
  </div>
  <br>

  <div style="text-align:center">
    <span class="dot" onclick="currentSlide(1)"></span> 
    <span class="dot" onclick="currentSlide(2)"></span> 
    <span class="dot" onclick="currentSlide(3)"></span> 
  </div>

  <section id="about-me" class="container">
    <div style="text-align:center">
      <h2>
        AstroChat
    </h2>
    <p>
      Welcome to AstroChat, where the wonders of the universe come to life! 
      <br> Our mission is to be your go-to destination for exploring the vast realms 
      of space and uncovering the mysteries of the cosmos. Whether you're a seasoned 
      astronomer or a curious novice, we aim to ignite your passion for the cosmos 
      and provide a rich, educational experience.
      <br>
      <br>At AstroChat, we believe that understanding the universe enriches our lives 
       and fuels our collective curiosity.Through a combination of cutting-edge technology
       and a passion for space exploration, we bring you a one-of-a-kind platform where you
       can delve into the latest astronomical discoveries, engage with our interactive
       chatbot, and immerse yourself in the beauty of the cosmos.
       <br>
    <br>Join us on a journey through the galaxies, from the wonders of our own solar system
    to the farthest reaches of the observable universe. Whether you're here for educational
    purposes, the latest space news, or simply to marvel at the breathtaking visuals,
    AstroChat is your gateway to the cosmos.<br><br>
    </p>
    </div>
  </section>

  <footer>
    <p>Author: Eshparsi Gupta, Pankhuri Thakur, Soumya Dubey<br>
    <a href="astrochat">AstroChat</a></p>
  </footer>

</div>
  </svelte:body>
  