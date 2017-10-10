<template>
  <div>
    <md-layout class="press-logos" md-vertical-align="start">
      <md-layout md-flex="75" md-hide-small md-gutter="16" md-vertical-align="middle">
        <ul>
          <li>
            <img src="../assets/images/daily-telegraph.png" alt="" class="press-brand">
          </li>
          <li>
            <img src="../assets/images/apra-amcos.png" alt="" class="press-brand">
          </li>
          <li>
            <img src="../assets/images/tech-in-asia.png" alt="" class="press-brand">
          </li>
          <li>
            <img src="../assets/images/tunecore.png" alt="" class="press-brand">
          </li>
          <li>
            <img src="../assets/images/huffpost.png" alt="" class="press-brand">
          </li>
          <li>
            <img src="../assets/images/reverb.png" alt="" class="press-brand">
          </li>
        </ul>
      </md-layout>
    </md-layout>

    <md-layout class="press-logos" md-vertical-align="start" md-hide-medium-and-up md-col>
      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <img src="../assets/images/daily-telegraph.png" alt="" class="press-brand">
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <img src="../assets/images/apra-amcos.png" alt="" class="press-brand">
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <img src="../assets/images/tech-in-asia.png" alt="" class="press-brand">
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <img src="../assets/images/tunecore.png" alt="" class="press-brand">
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <img src="../assets/images/huffpost.png" alt="" class="press-brand">
      </md-layout>

      <md-layout md-flex="100" md-align="center" md-gutter="16">
        <img src="../assets/images/reverb.png" alt="" class="press-brand">
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
      opacity: 0.5;
    }
  }

  /* Desktops and laptops ----------- */
  @media only screen  and (min-width : 961px) {
    .press-logos {
      padding: 35px 70px 25px;
      white-space: nowrap;
    }

    .press-brand {
      fill: #567483;
      padding-right: 45px;
      opacity: 0.5;
    }
  }




</style>
