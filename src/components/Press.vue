<template>
  <div>
    <md-layout class="press-logos" md-hide-small md-vertical-align="start">
      <md-layout md-flex="80" md-gutter="16" md-vertical-align="middle" class="space-between">
          <md-layout md-align="center">
            <a href="http://www.dailytelegraph.com.au/entertainment/sydney-confidential/hunters-and-connectors/news-story/d93aa0df090be0fd1e7720d51b849870?nk=6d68ac5cbb69a43c5229e8c4753bae1f-1507651072" target="_blank">
              <img src="../assets/images/daily-telegraph.png" alt="" class="press-brand">
            </a>
          </md-layout>
          <md-layout md-align="center">
            <a href="http://apraamcos.com.au/news/2017/april/music-and-tech-how-copyright-fuels-innovation/" target="_blank">
              <img src="../assets/images/apra-amcos.png" alt="" class="press-brand">
            </a>
          </md-layout>
          <md-layout md-align="center">
            <a href="https://www.techinasia.com/talk/rock-star-built-tinder-musicians" target="_blank">
              <img src="../assets/images/tech-in-asia.png" alt="" class="press-brand">
            </a>
          </md-layout>
          <md-layout md-align="center">
            <a href="http://www.tunecore.com/blog/2016/06/interview-josh-simons-on-vampr-the-new-collaboration-app-for-artists.html" target="_blank">
              <img src="../assets/images/tunecore.png" alt="" class="press-brand">
            </a>
          </md-layout>
          <md-layout md-align="center">
            <a href="https://www.huffingtonpost.com/entry/for-former-busker-ed-sheeran-and-for-other-undiscovered_us_5908e078e4b05279d4edc07b" target="_blank">
              <img src="../assets/images/huffpost.png" alt="" class="press-brand">
            </a>
          </md-layout>
          <md-layout md-align="center">
            <a href="https://reverb.com/news/3-apps-for-easier-musical-collaboration?utm_campaign=1612019_blogappsforcollab" target="_blank">
              <img src="../assets/images/reverb.png" alt="" class="press-brand">
            </a>
          </md-layout>

      </md-layout>
    </md-layout>

    <md-layout class="press-logos" md-vertical-align="start" md-hide-medium-and-up md-col>
      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <a href="http://www.dailytelegraph.com.au/entertainment/sydney-confidential/hunters-and-connectors/news-story/d93aa0df090be0fd1e7720d51b849870?nk=6d68ac5cbb69a43c5229e8c4753bae1f-1507651072" target="_blank">
          <img src="../assets/images/daily-telegraph.png" alt="daily-telegraph" class="press-brand">
        </a>
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <a href="http://apraamcos.com.au/news/2017/april/music-and-tech-how-copyright-fuels-innovation/" target="_blank">
          <img src="../assets/images/apra-amcos.png" alt="apra-amcos" class="press-brand">
        </a>
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <a href="https://www.techinasia.com/talk/rock-star-built-tinder-musicians" target="_blank">
          <img src="../assets/images/tech-in-asia.png" alt="tech-in-asia" class="press-brand">
        </a>
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <a href="http://www.tunecore.com/blog/2016/06/interview-josh-simons-on-vampr-the-new-collaboration-app-for-artists.html" target="_blank">
          <img src="../assets/images/tunecore.png" alt="tunecore" class="press-brand">
        </a>
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <a href="https://www.huffingtonpost.com/entry/for-former-busker-ed-sheeran-and-for-other-undiscovered_us_5908e078e4b05279d4edc07b" target="_blank">
          <img src="../assets/images/huffpost.png" alt="huffpost" class="press-brand">
        </a>
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <a href="https://reverb.com/news/3-apps-for-easier-musical-collaboration?utm_campaign=1612019_blogappsforcollab" target="_blank">
          <img src="../assets/images/reverb.png" alt="reverb" class="press-brand">
        </a>
      </md-layout>
    </md-layout>
  </div>
</template>

<script>
export default {
  name: 'press',
  data() {
    return {
      press: 'Welcome to Your Vue.js App',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* Mobile Styles ------------------ */
  @media only screen and (max-width : 960px) {
    .press-logos {
      padding: 15px 30px 25px;
    }

    .press-brand {
      fill: #567483;
      margin: 20px;
      opacity: 0.75;
    }
  }

  /* Desktops and laptops ----------- */
  @media only screen  and (min-width : 961px) {
    .press-logos {
      padding: 35px 100px 25px;
      white-space: nowrap;
    }

    .press-brand {
      text-align: center;
      fill: #567483;
      opacity: 0.75;
    }
  }

  .space-between {
    -webkit-box-pack: justify;
    justify-content: space-between;
    align-items: center;
    align-content: center;
    display: flex;
  }



</style>
