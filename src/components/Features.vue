<template>
    <md-layout class="features" md-align="center" md-flex md-gutter="40" md-row>
        <md-layout md-flex-small="100" md-align="center" md-flex="30">
          <div class="featurette">
            <img src="../assets/images/discover.png" alt="" class="icon">
            <h1>{{featureOne.title}}</h1>
            <p>{{featureOne.description}}</p>
          </div>
        </md-layout>

        <md-layout md-flex-small="100" md-align="center" md-flex="30">
          <div class="featurette">
            <img src="../assets/images/connect.png" alt="" class="icon">
            <h1>{{featureTwo.title}}</h1>
            <p>{{featureTwo.description}}</p>
          </div>
        </md-layout>

        <md-layout md-flex-small="100" md-align="center" md-flex="30">
          <div class="featurette">
            <img src="../assets/images/collaborate.png" alt="" class="icon">
            <h1>{{featureThree.title}}</h1>
            <p>{{featureThree.description}}</p>
          </div>
        </md-layout>
  </md-layout>
</template>

<script>
export default {
  name: 'features',
  data() {
    return {
      featureOne: {
        title: 'Discover',
        description: 'Find musicians, industry and music lovers near you. Build your profile with Soundcloud and YouTube.',
      },
      featureTwo: {
        title: 'Connect',
        description: 'See common musical interests and make new connections by swiping right on a profile.',
      },
      featureThree: {
        title: 'Collaborate',
        description: 'Chat securely with your new connections and get started on a new musical collaboration!',
      },
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* Mobile Styles ------------------ */
  @media only screen and (max-width : 960px) {
    .features {
      padding: 15px 30px 25px;
    }

    .featurette {
      margin: 30px 20px;
    }
  }

  /* Desktops and laptops ----------- */
  @media only screen  and (min-width : 961px) {
    .features {
      padding: 35px 70px 25px;
    }

    .featurette {
      margin: 0 40px;
    }
  }

  h1 {
    color: #00e4b5;
  }

  p {
    text-align: center;
  }

  .features {
    background-color: #f7f8f9;
  }

  .featurette {
    text-align: center;
  }
</style>
