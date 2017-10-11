<template>
  <md-layout class="counters" md-align="center" md-vertical-align="center" md-flex md-gutter="40" md-row>

      <md-layout md-flex-small="100" md-flex="30" md-align="center">
        <div class="featurette">
          <h1>{{parseInt(totals.total01).toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h1>
          <p>{{counterOne.label}}</p>
        </div>
      </md-layout>

      <md-layout md-hide-small md-flex="5" md-align="center">
        <img src="../assets/images/vertical-rule.png" />
      </md-layout>

      <md-layout md-flex="100" md-hide-medium-and-up md-align="center">
        <hr />
      </md-layout>

      <md-layout md-flex-small="100" md-flex="30" md-align="center">
        <div class="featurette">
          <h1>{{parseInt(totals.total02).toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",")}}</h1>
          <p>{{counterTwo.label}}</p>
        </div>
      </md-layout>

      <md-layout md-flex="5" md-hide-small md-align="center">
        <img src="../assets/images/vertical-rule.png" />
      </md-layout>

      <md-layout md-flex="100" md-hide-medium-and-up md-align="center">
        <hr />
      </md-layout>

      <md-layout md-flex-small="100" md-flex="30" md-align="center">
        <div class="featurette">
          <h1>{{parseInt(totals.total03)}}</h1>
          <p>{{counterThree.label}}</p>
        </div>
      </md-layout>
    </md-layout>
</template>

<script>
import { TweenMax } from 'gsap';

const totals = {
  total01: 2248223,
  total02: 456584,
  total03: 166,
};

const countUp = () => {
  const count = parseInt(Math.random() * 8, 0);
  TweenMax.to(totals, 1, { total01: `+=${count}` });
  TweenMax.to(totals, 1, { total02: `+=${count}`, delay: 0.5, onComplete: countUp });
};

window.addEventListener('load', () => {
  countUp();
});

export default {
  name: 'counters',
  data() {
    return {
      totals,
      counterOne: {
        label: 'Swipes on Vampr',
        total: totals.total01,
      },
      counterTwo: {
        label: 'Connections made',
        total: totals.total02,
      },
      counterThree: {
        label: 'Countries worldwide',
        total: totals.total03,
      },
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  /* Mobile Styles ------------------ */
  @media only screen and (max-width : 960px) {
    .featurette {
      margin: 40px 0;
    }
  }

  /* Desktops and laptops ----------- */
  @media only screen  and (min-width : 961px) {

  }

  h1 {
    margin:0;
    font-size: 46px;
    font-weight: 400;
  	line-height: 1.0;
    color: #00e4b5;
  }

  p {
    margin: 0;
    font-size: 16px;
  	line-height: 1.5;
    color: #567483;
  }

  .counters {
    padding: 35px 100px 35px;
    background-color: #eef1f2;
    color: #fff;
  }

  .featurette {
    text-align: center;
  }

  hr {
    width: 30%;
    border-color: #ccc;
    border-style: solid;
    border-bottom: none;
  }
</style>
