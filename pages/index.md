---
layout: home
title: Home
permalink: /
weight: 0
---

 <head>
    <style>
        .slideshow-container {
            max-width: 100%;
            position: relative;
            margin: auto;
        }
        .mySlides {
            display: none;
            width: 100%;
            height: 100%;
        }
        .active-slide {
            height: 10px;
            width: 160px;
            margin: 0 2px;
            background-color: #4682B4; /* Change to blue-grey when active-slide */
            display: inline-block;
            transition: background-color 0.6s ease;
            opacity: 1;
            cursor: pointer;
        }
        .inactive-slide {
            height: 10px;
            width: 160px;
            margin: 0 2px;
            background-color: #bbb;
            display: inline-block;
            transition: background-color 0.6s ease;
            opacity: 0.75;
            cursor: pointer;
        }
        .line-container {
            position: absolute;
            bottom: 10%;
            width: 100%;
            text-align: center;
        }
/* Stile für den Header, die Beschreibung und den Button */
        .header-container {
            position: absolute;
            left: 50px;
            top: 50%;
            transform: translateY(-50%);
            padding: 20px;
            color: white;
            width: 500px;
        }
        .header-title {
            font-size: 2em;
            margin-bottom: 10px;
        }
        .header-description {
            margin-bottom: 20px;
        }
.btn {
  display: inline-block;
  font-weight: 400;
  text-align: center;
  white-space: nowrap;
  vertical-align: middle;
  user-select: none;
  border: 1px solid transparent;
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  line-height: 1.5;
  border-radius: 0.25rem;
  transition: color 0.15s ease-in-out, background-color 0.15s ease-in-out, border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
  cursor: pointer;
}

/* Bootstrap-ähnliche primäre Button-Farbe */
.btn-primary {
  color: #fff;
  background-color: #473CFF;
  border-color: #473CFF;
}

/* Bootstrap-ähnliche Hover- und Focus-Effekte */
.btn-primary:hover, .btn-primary:focus {
  color: #fff;
  background-color: #6D64FF;
  border-color: #6D64FF;
}

.btn-white {
  color: #000;
  background-color: #fff;
  border-color: #ccc;
}

/* Bootstrap-ähnliche Hover- und Focus-Effekte */
.btn-white:hover, .btn-white:focus {
  color: #000;
  background-color: #ddd;
  border-color: #bbb;
}

/* Bootstrap-ähnliche aktive und gedrückte Effekte */
.btn-primary:active {
  color: #fff;
  background-color: #544AFF;
  border-color: #544AFF;
  box-shadow: 0 0.2rem 0.5rem rgba(167, 7, 7, 0.5);
}
/* Bootstrap-ähnliche aktive und gedrückte Effekte */
.btn-white:active {
  color: #000;
  background-color: #aaa;
  border-color: #777;
  box-shadow: 0 0.2rem 0.5rem rgba(150, 150, 150, 0.5);
}

/* Bootstrap-ähnliche deaktivierte Button-Stile */
.btn:disabled {
  color: #fff;
  background-color: #6c757d;
  border-color: #6c757d;
  cursor: not-allowed;
}
    </style>
</head>
<body>
    <div class="slideshow-container">
        <div class="mySlides">
            <img src="https://cdn2.unrealengine.com/Fortnite%2Fblog%2Fcreative%2FCM07_News_Featured_CreativeMode_Announce-1920x1080-f2b3606efe82d43a4a89ba8efbb00b630641e754.jpg" style="width:100%; height:100%">
<div class="header-container">
                <div class="header-title">CREATIVE</div>
                <div class="header-description">Creative is now available!</div>
                <a class="btn btn-primary" href="https://tfngamesofficial.github.io/devcreate/news/">Learn more</a>
            </div>
        </div>
        <div class="mySlides">
            <img src="https://cdn2.unrealengine.com/fortnite-home-page-battle-pass-promo-slide-desktop-1920x1080-6657f41ee1bd.jpg" style="width:100%; height:100%">
         <div class="header-container">
                <div class="header-title">Season 1: Dimensional </div>
                <div class="header-description">A new Season Pass is here! Season 1 is now here and brings new stuff.</div>
                <a class="btn btn-white" href="https://tfngamesofficial.github.io/devnite/battle-royale/">Check it out</a>
            </div>
        </div>
        <div class="mySlides">
            <img src="https://cdn2.unrealengine.com/fortnite-no-build-battle-royale-desktop-1920x1080-b010abfc1691.jpg" style="width:100%; height:100%">
         <div class="header-container">
                <div class="header-title">Highgames LTM</div>
                <div class="header-description">A new LTM is available! The Highgames series contains 4 LTMs. Visit Discover site for details.</div>
                <a class="btn btn-success" href="/discover/">Show me</a>
            </div>
        </div>
        <div class="line-container">
            <span class="inactive-slide"></span> 
            <span class="inactive-slide"></span> 
            <span class="inactive-slide"></span>
        </div>
    </div>
<script>
    var slideIndex = 0;
    showSlides();
    function showSlides() {
        var i;
        var slides = document.getElementsByClassName("mySlides");
        var lines = document.getElementsByClassName("inactive-slide");
        for (i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";  
        }
        slideIndex++;
        if (slideIndex > slides.length) {slideIndex = 1}    
        for (i = 0; i < lines.length; i++) {
            lines[i].className = lines[i].className.replace(" active-slide", "");
            lines[i].style.backgroundColor = "#bbb"; // Farbe der inaktiven Linien
        }
        slides[slideIndex-1].style.display = "block";  
        lines[slideIndex-1].className += " active-slide";
        lines[slideIndex-1].style.backgroundColor = "#4682B4"; // Farbe der aktiven Linie
        setTimeout(showSlides, 5000); // Change image every 5 seconds
    }
    function currentSlide(n) {
        var i;
        var slides = document.getElementsByClassName("mySlides");
        var lines = document.getElementsByClassName("inactive-slide");
        for (i = 0; i < slides.length; i++) {
            slides[i].style.display = "none";  
        }
        for (i = 0; i < lines.length; i++) {
            lines[i].className = lines[i].className.replace(" active-slide", "");
            lines[i].style.backgroundColor = "#bbb"; // Farbe der inaktiven Linien
        }
        slides[n-1].style.display = "block";  
        lines[n-1].className = " active-slide";
        lines[n-1].style.backgroundColor = "#4682B4"; // Farbe der aktiven Linie
        slideIndex = n;
    }
</script>

</body>
