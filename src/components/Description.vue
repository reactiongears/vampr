<template>
  <div class="description">
  <md-layout md-hide-medium-and-up md-gutter="32">
    <h1>{{header}}</h1>
  </md-layout>

  <md-layout md-vertical-align="start">
    <md-layout md-gutter="16" md-flex-small="55" md-flex="75" md-vertical-align="start">
      <md-layout md-hide-small>
        <h1>{{header}}</h1>
      </md-layout>
      <p>{{copy}}</p>
    </md-layout>
    <md-layout>
      <img id="iphone" src="../assets/images/iphone.png" class="iphoneBase" />
      <img id="iphone01" src="../assets/images/iphone01.png" class="iphone" />
      <img id="iphone02" src="../assets/images/iphone02.png" class="iphone" />
      <img id="iphone03" src="../assets/images/iphone03.png" class="iphone" />
    </md-layout>
  </md-layout>

</div>
</template>

<script>
import { TweenMax } from 'gsap';

const shuffleiPhone = () => {
  TweenMax.to('#iphone01', 1, { opacity: 1 });
  TweenMax.to('#iphone01', 1, { opacity: 0, delay: 3 });
  TweenMax.to('#iphone02', 1, { opacity: 1, delay: 3 });
  TweenMax.to('#iphone02', 1, { opacity: 0, delay: 6 });
  TweenMax.to('#iphone03', 1, { opacity: 1, delay: 6 });
  TweenMax.to('#iphone03', 1, { opacity: 0, delay: 9, onStart: shuffleiPhone });
};

window.addEventListener('load', () => {
  shuffleiPhone();
});

export default {
  name: 'description',
  data() {
    return {
      header: 'Great things happen when people connect',
      copy: 'Who you know or where you live are no longer barriers to getting on with playing and making music. Vampr helps you discover, connect and collaborate with musicians, the music industry and music lovers alike.',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* Mobile Styles ------------------ */
  @media only screen and (max-width : 960px) {
    .description {
      padding: 15px 30px 25px;
    }

    p {
      font-size: 18px;
      font-weight: 400;
    	line-height: 1.19;
    }

    .iphoneBase,
    .iphone {
      top: 552px;
      right: 20px;
      width: 130px;
    }
  }

  /* Desktops and laptops ----------- */
  @media only screen  and (min-width : 961px) {
    .description {
      padding: 35px 100px 25px;
    }

    p {
      font-size: 20px;
    	font-weight: 400;
    	line-height: 1.19;
    }

    .iphoneBase,
    .iphone {
      top: 490px;
      right: 100px;
    }
  }

  h1 {
    margin:0;
    font-size: 30px;
  	font-weight: bold;
  	line-height: 1.0;
    margin-left: -10px;
  }

  .description {
    background-color: #00e4b5;
    color: #fff;
  }

  .iphone {
    position: absolute;
    height: auto;
    opacity: 0;
    z-index: 100;
  }

  .iphoneBase {
    position: absolute;
    height: auto;
    z-index: 100;
  }
</style>
