<template>
  <md-layout class="footer" md-gutter="40" md-row>

    <md-layout md-hide-medium-and-up md-flex="100" md-align="center">
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

      <md-layout md-flex-small="100" md-flex="70" md-align="start">
        <div class="legal-copy">
          {{legal}}
            &nbsp;|&nbsp;
            <a href="#terms">Terms &amp; Conditions</a>
            &nbsp;|&nbsp;
            <a href="#privacy">Privacy</a>
            &nbsp;|&nbsp;
            <a href="http://blog.vampr.me" class="nav-item" target="_blank">  Blog</a>
            &nbsp;|&nbsp;
            <a href="http://press.vampr.me" class="nav-item" target="_blank">Press</a>
            &nbsp;|&nbsp;
            <a href="mailto:support@vampr.me" class="nav-item" target="_blank">Contact</a>
        </div>
      </md-layout>

    <md-layout md-hide-small md-flex="30" md-align="end" md-vertical-align="start">

        <a href="http://www.facebook.com/vamprapp" target="_blank">
          <img src="../assets/icons/social/grey/facebook-faded-grey.svg" class="social-item" alt="">
        </a>

        <a href="http://www.twitter.com/vamprapp" target="_blank">
          <img src="../assets/icons/social/grey/twitter-faded-grey.svg" class="social-item" alt="">
        </a>

        <a href="http://www.instagram.com/vamprapp" target="_blank">
          <img src="../assets/icons/social/grey/instagram-faded-grey.svg" class="social-item" alt="">
        </a>

    </md-layout>
  </md-layout>

</template>

<script>
export default {
  name: 'footer',
  data() {
    return {
      legal: '© Vampr Pty Ltd 2017',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @media only screen and (max-width : 960px) {
    .footer {
      padding: 15px 30px 35px;
    }

    .legal-copy {
      margin: 20px 0 0;
    }
  }

  /* Desktops and laptops ----------- */
  @media only screen  and (min-width : 961px) {
    .footer {
      padding: 35px 70px 35px;
    }

    .legal-copy {
      margin: 0;
    }
  }

  a {
    color: #567483 !important;
  }

  a:hover {
    text-decoration: none !important;
  }

  .footer {
    background-color: #f7f8f9;
    color: #fff;
  }

  .legal-copy {
    font-size: 12px;
  	line-height: 2.5;
    color: #567483;
  }

  .social-item {
    width:35px;
    margin-left: 20px;
  }
</style>
