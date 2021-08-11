<template lang="html">
  <section class="containerSlider" v-if="banners">
      <div v-for="banner in banners" :key="banner.id" class="containerBanner">
        <a :href="$screen.width > 1023 ? banner.dimensoes.desktop.link : banner.dimensoes.mobile.link" :id="`banner-bannerPrincipal-${banner.id}`">
          <img :src="banner.dimensoes.desktop[tipoImg.banner]" :alt="banner.nome" class="banner-desk" v-if="$screen.width > 1023">
          <img :src="banner.dimensoes.mobile[tipoImg.banner]" :alt="banner.nome" class="banner-mob" v-else>
        </a>
      </div>
  </section>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  props: {
      banners: Array
  },
  computed: {
    ...mapGetters(['tipoImg'])
  }
}
</script>

<style lang="css" scoped>
.containerSlider {
  /*min-height: 540px;*/
  background-color: #DDE8EE;
  background-repeat: no-repeat;
  background-position: -600%;
  background-size: 80%;
  background-image: linear-gradient(90deg, #dee9ee 0%, #d3e0e8 50%, #dee9ee 100%);
  animation: loading infinite 1.5s;
  max-width: 1920px;
  margin: 0 auto;
}
</style>
