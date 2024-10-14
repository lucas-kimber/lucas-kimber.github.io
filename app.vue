<template>
  <div class="app">
    <NuxtRouteAnnouncer />
    <div class="panel">
      <div class="b1"></div>
      <div class="b2"></div>
      <div class="b3"></div>
      <div class="p1"></div>
      <div class="p2"></div>
      <div class="p3"></div>
    </div>
    <div class="sidebar">
      <Logo /> <Socials />
      <p class="intro">I am a Computer Scientist with an interest in software development, refined by my work experience in developer roles. My
        BSc has equipped me with the fundamental principles of CS and software engineering, and now I am growing this
        knowledge with a Masters at UCL. Following this, I hope to utilise my skills to work on emerging technologies in
        industry.</p>

      <Nav />

      <NuxtPage />
    </div>
  </div>
</template>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

:root {
  --accent: white;
  --shadow: white;
}

body {
  background-color: black;
  background-image: url(./public/background.jpg);
  background-attachment: fixed;
  background-position: -150px center;
  background-size: auto 100%;
  position: fixed;
  overflow: hidden;
  margin: 0;
  font-family: "Poppins", sans-serif;
  color: white;
}

@media (min-aspect-ratio: 16/9) {
  body {
    background-position: left center;
  }
}

.sidebar {
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 47%;
  z-index: 10;
  padding-top: 50px;
  padding-right: 35px;
  max-height: 100vh;
}

.content-scroll-box {
  padding-bottom: 15px;
}

.panel {
  position: relative;
  overflow: hidden;
  width: 100vw;
  height: 100vh;
  top: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0,0,0,0.6);
  max-height: 100vh;
  
  
  .p1,.p2,.p3 {
    background-color: rgb(20,20,20);
    position: absolute;
    z-index: 4;
  }
  .b1,.b2,.b3 {
    position: absolute;
    background-color: var(--accent);
    box-shadow: 0 0 15px 5px var(--shadow);
    z-index: 1;
  }

  .p1, .b1 {
    right: 0;
    top: 0;
    bottom: 0;
    left: 45%;
  }
  
  .b1 {
    left: 45%;
    transform: rotate(3deg);
    z-index: 2;
  }
  .p2, .b2 {
    top: -10%;
    right: 46%;
    transform: rotateZ(9deg) skew(5deg, 53deg);
    width: 12%;
    height: 69%;
  }
  .b2 {
    top: -9%;
    right: 46.5%;
  }
  
  .p3, .b3 {
    top: 73%;
    right: 51%;
    transform: rotateZ(346deg) skew(343deg, 313deg);
    width: 7%;
    height: 31%;
  }
  .b3 {
    top: 73%;
    right: 51.3%;
  }
}

@media screen and (max-width: 340px){
  .socials {
    text-align: center;
  }
}

@media screen and (max-width: 768px) {
  body {
    background-position: left top;
    background-size: 130% auto;
  }
  .panel {
    .p3, .b3 {
      display: none;
    }
    .p1, .b1 {
      left: 0;
      right: 0;
      bottom: 0;
      top: 200px;
      position: fixed;
    }
    .b1 {
      left: -30px;
      transform: rotate(2deg);
      top: 189px;
    }
    .b2, .p2 {
      transform: rotateZ(290deg) skew(5deg, 53deg);
      width: 70px;
      height: 176px;
      top: 110px;
      right: 0px;
      position: fixed;
    }
    .p2 {
      top: 120px;
    }

  }

  .sidebar {
    left: 15px;
    right: 15px;
    top: 220px;
    padding-right: 0;
    padding-top: 0px;
    overflow: scroll;

    .brand {
      scale: 0.8;
      transform: translateX(-35px) translateY(-20px);
      width: 70%;
      margin-bottom: 0;
    }

    .socials {
      float: none;
      margin-top: 24px;
      vertical-align: top;
    }

    .intro {
      text-align: justify;
      font-size: 14px;
    }


  }
}

</style>