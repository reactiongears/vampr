<template>
    <div class="header">
      <div class="header-content">
        <md-layout class="nav-bar" md-align-small="center" md-vertical-align="start">
          <md-layout md-flex-small="100" md-align-small="center" md-align="start" md-flex="45" md-gutter="16" md-vertical-align="start">
            <a href="http://www.vampr.me" class="nav-item" target="_blank">Home</a>

            <a href="http://blog.vampr.me" class="nav-item" target="_blank">Blog</a>

            <a href="http://press.vampr.me" class="nav-item" target="_blank">Press</a>

            <a href="mailto:support@vampr.me" class="nav-item" target="_blank">Contact</a>
          </md-layout>

          <md-layout md-flex="20" md-align="center" md-hide-small>
            <img class="logo" src="../assets/icons/logo.svg" />
          </md-layout>

          <md-layout md-flex="33" md-align="end" md-vertical-align="start" md-hide-small>

              <a href="http://www.facebook.com/vamprapp" target="_blank">
                <img src="../assets/icons/social/teal/facebook-teal.svg" class="social-item" alt="">
              </a>

              <a href="http://www.twitter.com/vamprapp" target="_blank">
                <img src="../assets/icons/social/teal/twitter-teal.svg" class="social-item" alt="">
              </a>

              <a href="http://www.instagram.com/vamprapp" target="_blank">
                <img src="../assets/icons/social/teal/instagram-teal.svg" class="social-item" alt="">
              </a>

          </md-layout>
        </md-layout>

        <md-layout md-flex="33" md-align="center" md-hide-medium-and-up>
          <img class="logo" src="../assets/icons/logo.svg" />
        </md-layout>

        <md-layout>
          <md-layout md-gutter="16" md-flex="33">
            <div class="hero-text">
              <h1 style="color: #9f1be6;">DISCOVER</h1>
              <h1 style="color: #00e4b5;">CONNECT</h1>
              <h1 style="color: #fff;">COLLABORATE</h1>
            </div>
          </md-layout>
        </md-layout>

        <md-layout>
          <md-layout md-row md-gutter="16" md-align="start" class="downloads">

                <a href="https://itunes.apple.com/app/vampr/id1069819177" target="_blank">
                  <img src="../assets/images/download-apple.png" class="download-app" alt="iTunes">
                </a>
                <a href="https://play.google.com/store/apps/details?id=me.vampr.android" target="_blank">
                  <img src="../assets/images/download-google.png" class="download-app" alt="Google Play">
                </a>

          </md-layout>
        </md-layout>

      </div>
    </div>
</template>

<script>
export default {
  name: 'header',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
    };
  },
};
</script>

<style scoped>
  /* Mobile Styles ------------------ */
  @media only screen and (max-width : 960px) {
    .header-content {
      padding: 30px;
    }

    .header {
      background-size:cover;
    }

    .logo {
      margin-top: 15px;
      width: 80px;
    }

    .nav-item {
      padding: 0px;
    }

    .hero-text {
      font-family: 'DinCond';
      font-size: 26px;
    }

    .download-app {
      width: 100px;
    }
  }

  /* Desktops and laptops ----------- */
  @media only screen  and (min-width : 961px) {
    .header-content {
      padding: 70px;
    }

    .hero-text {
      font-family: 'DinCond';
      font-size: 46px;
    }

    .nav-item {
      padding-right: 20px;
    }

    .download-app {
      width: 200px;
    }
  }

  a:hover {
    text-decoration: none !important;
  }

  .download-app {
    margin-right: 15px;
    height: auto;
  }

  .header {
    background-position-x: center;
    background-position-y: start;
    background-color: #000;
    background-repeat: no-repeat;
    background-image: url("../assets/images/hero-dk-edges.jpg");
  }

  .social-item {
    width:35px;
    margin-left: 20px;
  }

  .nav-item {
    font-size: 16px;
    font-weight: 400;
    color: #00e4b5 !important;
    margin: 0 10px;
  }

  .logo {
    height: 150px;
  }
  
  @font-face {
    font-family: 'DinCond';
    src: url('../assets/fonts/DINWeb-CondBold.eot'); /* IE9 Compat Modes */
    src: url('../assets/fonts/DINWeb-CondBold.eot') format('embedded-opentype'), /* IE6-IE8 */
         url('../assets/fonts/DINWeb-CondBold.woff') format('woff'),
         url('../assets/fonts/DINWeb-CondBold.ttf')  format('truetype')
  }
</style>
