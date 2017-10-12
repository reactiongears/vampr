<template>
  <div class="featured-artist">
    <md-layout md-align="center">
      <md-layout class="center" md-flex>
        <h1>{{header}}</h1>
      </md-layout>
    </md-layout>


    <md-layout md-gutter="16" md-vertical-align="center" md-align="center">

      <md-layout md-flex-small="40" md-flex="15">
        <div>
          <img src="../assets/images/artist-cover-alex-ava.png" class="featured-artist-img" alt="">
        </div>
      </md-layout>

      <md-layout md-flex-small="60" md-flex="25">
        <h2>{{artist}}</h2>
        <p>{{copy}}</p>
        <a class="cta" :href="href">{{cta}}</a>
      </md-layout>

      <md-layout md-flex="45" md-hide-small>
        <iframe class="video" :src="src" frameborder="0" allowfullscreen=""></iframe>
      </md-layout>

    </md-layout>

    <md-layout md-flex md-hide-medium-and-up md-align="center" class="center">
      <iframe class="video" :src="src" frameborder="0" allowfullscreen=""></iframe>
    </md-layout>
  </div>
</template>

<script>
export default {
  name: 'featuredArtist',
  data() {
    return {
      header: 'Vampr featured artist',
      artist: 'ALEX AVA',
      copy: 'After years of struggling to find her creative voice, Scotland’s Alex AVA used Vampr to connect with Orlando producer, Vncnzo. Together they are now gearing up to release an entire EP!',
      cta: 'Connect with her on Vampr',
      href: 'https://id.vampr.me/s/be865e2a-cd58-4141-bb11-8f2d6024a264',
      src: 'https://www.youtube.com/embed/TZ9rHVDBqbg',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* Mobile Styles ------------------ */
  @media only screen and (max-width : 960px) {
    .featured-artist {
      padding: 15px 15px 45px;
      min-height:400px;
    }

    .video {
      margin-top: 30px;
    }

    .featured-artist-img {
      width: 150px;
    }

    p {
      font-size: 12px;
    	line-height: 1;
    }
  }

  /* Desktops and laptops ----------- */
  @media only screen  and (min-width : 961px) {
    .featured-artist {
      padding: 35px 100px 45px;
      min-height:400px;
    }

    .featured-artist-img {
      width: 200px;
    }

    p {
      font-size: 14px;
    	line-height: 1.19;
    }
  }

  h1 {
    text-align: center;
    margin:0 0 30px;
    font-size: 30px;
  	font-weight: bold;
  	line-height: 1.0;
    color: #00e4b5;
    width: 100%;
  }

  h2 {
    font-weight: bold;
    margin: 0 0 0px;
    color: #567483;
  }

  p {
    color: #567483;
    font-size: 14px;
  	line-height: 1.19;
  }

  a:hover{
    text-decoration: none;
  }

  a {
    color: #567483 !important;
  }

  .center {
    text-align: center;
  }

  .cta {
    color: #567483 !important;
    font-size: 14px;
    font-weight: bold;
    cursor: pointer;
  }

  .featured-artist {
    background-color: #eef1f2;
    min-height:400px;
  }

  .featured-artist-img {
    height: auto;
  }

  .video {
    height: 280px;
    width: 500px;
  }
</style>
