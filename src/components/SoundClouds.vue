<template>
  <div class="sound-clouds">
    <md-layout md-align="center">
      <md-layout class="center" md-flex>
        <h1>{{header}}</h1>
      </md-layout>
    </md-layout>


    <md-layout md-gutter="16" md-vertical-align="center">
      <md-layout md-flex>
        <div id="sctracks">
        <ol id="tracksOL">
          <li v-for="track in tracks">
            <button :id="track.id" class="album-btn" v-on:click="playTrack(track.id)">
              <div class="img-container">
                <img :id="track.id + '_stop'" class="stop" src="../assets/images/stop.png" />
                <img class="play" src="../assets/images/play.png" />
                <img class="album-art" :src="track.artwork_url" />
              </div>
            </button>
          </li>
        </ol>
      </div>
      </md-layout>
    </md-layout>

    <md-layout md-align="center">
      <md-layout md-vertical-align="center" class="nowrap" md-align="center" md-flex="100">

        <button v-on:click="scrollLeft()">
          <img class="scroll-arrow" src="../assets/icons/left-arrow.svg" alt="Left" />
        </button>

        <button v-on:click="scrollRight()">
          <img class="scroll-arrow" src="../assets/icons/right-arrow.svg" alt="Right" />
        </button>

      </md-layout>
    </md-layout>

  </div>
</template>

<script>
  import { TweenMax } from 'gsap';

  const SC = require('soundcloud');

  SC.initialize({
    client_id: 'JlZIsxg2hY5WnBgtn3jfS0UYCl0K8DOg',
  });

  const TRACKS = [];
  let currentPayingTrack;
  let activeButton;

  const stopTrack = () => {
    SC.sound.kill();
  };

  const playTrack = (trackId) => {
    if (trackId === currentPayingTrack) {
      activeButton.style.display = 'none';
      activeButton = null;
      currentPayingTrack = null;
      stopTrack();
      return;
    }

    if (currentPayingTrack) {
      activeButton = document.getElementById(`${currentPayingTrack}_stop`);
      activeButton.style.display = 'none';
    }

    SC.stream(`/tracks/${trackId}`).then((sound) => {
      SC.sound = sound;
      SC.sound.play();
      currentPayingTrack = trackId;
      activeButton = document.getElementById(`${trackId}_stop`);
      activeButton.style.display = 'block';
      console.log(activeButton);
    });
  };

  SC.get('/users/user-303148065/playlists').then((data) => {
    data[0].tracks.forEach((val) => {
      TRACKS.push(val);
    });
  });

  const scrollLeft = () => {
    TweenMax.to('#sctracks', 1, { scrollLeft: '-=500' });
  };

  const scrollRight = () => {
    TweenMax.to('#sctracks', 1, { scrollLeft: '+=500' });
  };


  export default {
    name: 'soundClouds',
    data() {
      return {
        header: 'Find a sound you like, connect and collaborate',
        tracks: TRACKS,
        playTrack,
        stopTrack,
        scrollLeft,
        scrollRight,
      };
    },
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1 {
    text-align: center;
    margin:0 0 30px;
    padding: 0 30px;
    font-size: 30px;
  	font-weight: bold;
  	line-height: 1.0;
    color: #00e4b5;
    width: 100%;
  }

  h2 {
    font-weight: bold;
    margin: 0 0 0px;
  }

  p {
    font-size: 14px;
  	line-height: 1.19;
  }

  a:hover{
    text-decoration: none !important;
  }

  a {
    color: #000 !important;
  }

  button {
    background: none;
    border: none;
    cursor: pointer;
  }

  .sound-clouds {
    padding: 55px 0 45px;
  }

  .album-art {
    border-radius: 100px;
    width: 130px;
    height: 130px;
    margin-right: 55px;
  }

  .img-container {
    position: relative;
  }

  .stop {
    display: none;
    position: absolute;
    z-index: 3;
    margin-top: 42px;
    margin-left: 42px;
    width: 43px;
    height: auto;
  }

  .play {
    position: absolute;
    z-index: 2;
    margin-top: 42px;
    margin-left: 42px;
    width: 43px;
    height: auto;
  }

  #sctracks {
    width: 100vw;
    overflow-y: scroll;
    -webkit-overflow-scrolling: touch;
    white-space: nowrap;
  }

  .scroll-arrow {
    margin: 0px 45px;
    padding-top: 8px;
    width: 18px;
    height: auto;
  }
</style>
