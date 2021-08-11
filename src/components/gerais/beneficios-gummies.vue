<template lang="html">
  <section class="famososRecomendam">
    <transition name="fadeNoDelay">
      <div id="famososRecomendam-video" v-if="video" @click="closeVideo()">
        <!--<div class="famososRecomendam-videoContainer" @click.stop="">
          <button type="button" name="button" class="famososRecomendam-video-close" @click="closeVideo()">
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" viewBox="0 0 21.9 21.9" enable-background="new 0 0 21.9 21.9" width="16px" height="16px">
              <path d="M14.1,11.3c-0.2-0.2-0.2-0.5,0-0.7l7.5-7.5c0.2-0.2,0.3-0.5,0.3-0.7s-0.1-0.5-0.3-0.7l-1.4-1.4C20,0.1,19.7,0,19.5,0  c-0.3,0-0.5,0.1-0.7,0.3l-7.5,7.5c-0.2,0.2-0.5,0.2-0.7,0L3.1,0.3C2.9,0.1,2.6,0,2.4,0S1.9,0.1,1.7,0.3L0.3,1.7C0.1,1.9,0,2.2,0,2.4  s0.1,0.5,0.3,0.7l7.5,7.5c0.2,0.2,0.2,0.5,0,0.7l-7.5,7.5C0.1,19,0,19.3,0,19.5s0.1,0.5,0.3,0.7l1.4,1.4c0.2,0.2,0.5,0.3,0.7,0.3  s0.5-0.1,0.7-0.3l7.5-7.5c0.2-0.2,0.5-0.2,0.7,0l7.5,7.5c0.2,0.2,0.5,0.3,0.7,0.3s0.5-0.1,0.7-0.3l1.4-1.4c0.2-0.2,0.3-0.5,0.3-0.7  s-0.1-0.5-0.3-0.7L14.1,11.3z" fill="#000000"/>
            </svg>
          </button>
          <canvas id="famososRecomendam-video-canvas" width="700" height="360"></canvas>
          <iframe id="famososRecomendam-video-iframe" :src="video"></iframe>
        </div>-->
      </div>
    </transition>
    <div class="container">
      <div class="row">
        <div class="col-12 noPaddingMob">
          <div class="famososRecomendam-sliderContainer">
            <div class="famososRecomendam-sliderContainer-slider" ref="famososRecomendamSlider">
              <div v-for="(famoso, i) in gummiesBene" :key="i">
                
                <div class="famososRecomendam-sliderContainer-slider-item">
                  <div class="famososRecomendam-sliderContainer-slider-item-img">
                    <img :src="require(`@/${famoso.img}`)" alt="">
                  </div>
                </div>

              </div>
            </div>
            <!--<div id="famososRecomendamSlider-nav" ref="famososRecomendamSliderNav" v-if="screenWidth > 767">
              <button type="button" name="button" class="prev">
                <svg viewBox="0 0 100 100"><path d="M 10,50 L 60,100 L 70,90 L 30,50  L 70,10 L 60,0 Z" class="arrow"></path></svg>
              </button>
              <button type="button" name="button" class="next">
                <svg viewBox="0 0 100 100"><path d="M 10,50 L 60,100 L 70,90 L 30,50  L 70,10 L 60,0 Z" class="arrow" transform="translate(100, 100) rotate(180) "></path></svg>
              </button>
            </div>-->
          </div>
          <router-link v-if="$route.path != '/produtos'" class="facaSeuPedido" to="/produtos">FAÇA SEU PEDIDO</router-link>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import {tns} from '@/../node_modules/tiny-slider/src/tiny-slider.js'
import {mapState} from 'vuex'

export default {
  props: {
    rmTitle: Boolean
  },
  data() {
    return {
      video: null
    }
  },
  methods: {
    openVideo(urlVideo) {
      this.video = urlVideo;
      document.body.style.overflow = 'hidden';
    },
    closeVideo() {
      this.video = null;
      document.body.style.overflow = '';
    }
  },
  computed: {
    ...mapState({
      screenWidth: state => state.screenWidth,
      gummiesBene: state => state.gummiesBene.gummiesBene
    })
  },
  created() {
    const interval = setInterval(() => {
      if (this.$refs.famososRecomendamSlider && this.$refs.famososRecomendamSlider.childElementCount == this.gummiesBene.length) {
        tns({
          container: this.$refs.famososRecomendamSlider,
          mouseDrag: true,
          items: 2,
          gutter: 8,
          slideBy: 'page',
          controlsContainer: this.$refs.famososRecomendamSliderNav,
          responsive: {
            '768': {
              gutter: 0,
              items: 4
            }
          }
        });
        clearInterval(interval);
      }
    }, 100);
  }
}
</script>

<style lang="css" scoped>
.tns-nav{
  display: none;
}
/* FAMOSOS RECOMENDAM */
.famososRecomendam{
  margin-top: 45px;
}
.famososRecomendam img{
  max-width: 100% !important;
}
.famososRecomendam-t1{
  font-size: 36px;
  color: #404040;
  font-weight: 500;
  text-align: center;
  margin-bottom: 0;
}
.famososRecomendam-t2{
  font-size: 15px;
  color: #888888;
  text-align: center;
  margin-bottom: 30px;
}
.famososRecomendam-sliderContainer{
  position: relative;
  margin-bottom: 30px;
}
#famososRecomendamSlider-nav button {
  background-color: #ff3e9b;
  height: 44px;
  width: 44px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 100%;
  position: absolute;
  top: calc(40% - 10px);
  border: none;
}
#famososRecomendamSlider-nav button svg {
  height: 26.39px;
  width: 26.39px;
  fill: #fff;
}
#famososRecomendamSlider-nav .prev {
  left: -55px;
}
#famososRecomendamSlider-nav .next {
  right: -55px;
}

.famososRecomendam-sliderContainer-slider-item{
  display: flex;
  margin: 0 auto;
  flex-direction: column;
  align-items: center;
  max-width: 260px;
}
.famososRecomendam-sliderContainer-slider-item-text{
  background-color: #ff3e9b;
  width: 100%;
  text-align: center;
  color: #fff;
  height: 60px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.famososRecomendam-sliderContainer-slider-item-text-t1{
  font-size: 15px;
}
.famososRecomendam-sliderContainer-slider-item-text-t2{
  font-size: 13px;
}
.famososRecomendam-sliderContainer-slider-item-img{
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}
.famososRecomendam-sliderContainer-slider-item-img-play{
  font-family: 'FontAwesome';
  font-size: 40px;
  color: #fff;
  opacity: 0.7;
  position: absolute;
  font-style: normal;
}
.famososRecomendam-sliderContainer-slider-item-img-play:hover{
  color: #ff3e9b;
  opacity: 1;
  transition: all 0.5s ease;
  cursor: pointer;
}
.famososRecomendam-sliderContainer-slider-item-img-play::before{
  content: "\f04b";
}
/* video */
#famososRecomendam-video{
  position: fixed;
  height: 100vh;
  width: 100vw;
  background-color: rgba(255, 255, 255, 0.5);
  top: 0;
  left: 0;
  z-index: 100;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 15px;
}
.famososRecomendam-videoContainer{
  position: relative;
  background-color: #fff;
  padding-top: 10px;
}
#famososRecomendam-video-canvas{
  max-width: 100%;
  opacity: 0;
}
#famososRecomendam-video-iframe{
  top: 0;
  left: 0;
  position: absolute;
  width: 100%;
  height: 100%;
  border: none;
}
.famososRecomendam-video-close{
  position: absolute;
  top: -26px;
  right: 0;
}

@media (max-width: 767px) {
  .famososRecomendam{
    overflow: hidden;
  }
  .famososRecomendam-t2{
    line-height: 1.3;
  }
  .noPaddingMob{
    padding: 0;
  }
  .famososRecomendam-sliderContainer-slider-item-text-t1 {
    font-size: 13px;
  }
}
</style>

<style>
  /* FAMOSOS RECOMENDAM */
  .famososRecomendam-sliderContainer .tns-nav {
    bottom: -55px;
    display: none;
  }
  .famososRecomendam-sliderContainer .tns-nav > button {
    border: none;
    background-color: #333;
    opacity: 0.25;
    margin: 0 8px;
  }
  .famososRecomendam-sliderContainer .tns-nav > button.tns-nav-active,
  .famososRecomendam-sliderContainer .tns-nav > button:hover {
    background-color: #333;
    opacity: 1;
  }
  @media (max-width: 767px) {
    .famososRecomendam-sliderContainer .tns-inner {
      padding-left: 7px;
      padding-right: 30px;
    }
    .famososRecomendam-sliderContainer .tns-nav {
      bottom: -35px;
    }
  }
</style>
