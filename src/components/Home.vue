<template>
  <div class="home">
    <PageHeader />
    <Description />
    <Press />
    <Features />
    <FeaturedArtist />
    <SoundClouds />
    <Counters />
    <Footer />
  </div>
</template>

<script>
import PageHeader from '@/components/Header';
import Description from '@/components/Description';
import Press from '@/components/Press';
import Features from '@/components/Features';
import FeaturedArtist from '@/components/FeaturedArtist';
import SoundClouds from '@/components/SoundClouds';
import Counters from '@/components/Counters';
import Footer from '@/components/Footer';

export default {
  name: 'home',
  components: {
    PageHeader,
    Description,
    Press,
    Features,
    FeaturedArtist,
    SoundClouds,
    Counters,
    Footer,
  },
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  html,body
  {
    width: 100%;
    height: 100%;
    margin: 0px;
    padding: 0px;
    overflow-x: hidden;
    -webkit-overflow-scrolling: touch;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px 0 0;
  }

  .center {
    text-align: center;
  }

  .nowrap {
    white-space: nowrap;
  }

  .md-theme-default :not(input):not(textarea)::selection {
    background: #ccc !important;
    color: #000 !important;
  }

  .img:not(.md-image) {
    height: inherit;
  }
</style>
