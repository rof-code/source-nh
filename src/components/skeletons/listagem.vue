<template lang="html">
  <div class="skeleton">
    <pitchbar v-if="$screen.width >= 1024" />
    <div class="flex-container align-middle noAnim noRadius" style="width: 100%; height: 230px; margin-bottom: 10px;">
      <div class="container noColor">
        <div class="row noColor" style="width: 100%;" v-if="$screen.width >= 1024">
          <div class="col-sm-12 col-lg-6 noColor large-offset-6">
            <div class="escuro" style="width: 245px; height: 24px; margin-bottom: 13px"></div>
            <div class="escuro" style="width: 100%; height: 12px; margin-bottom: 10px"></div>
            <div class="escuro" style="width: 100%; height: 12px; margin-bottom: 10px"></div>
            <div class="escuro" style="width: 100%; height: 12px; margin-bottom: 10px"></div>
            <div class="escuro" style="width: 270px; height: 12px; margin-bottom: 10px"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="container noColor">
      <div class="row noColor">
        <div class="col-12 noColor">
          <div class="escuro" style="width: 133px; height: 12px; margin-bottom: 20px"></div>
        </div>
      </div>
      <div class="row noColor">
        <div class="col-sm-12 col-lg-2 noColor" v-if="$screen.width >= 1024">
          <menuLateral />
        </div>
        <div class="col-sm-12 col-lg-10 noColor">
          <prods />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import '@/assets/css/skeleton.css'
export default {
  components: {
    prods: () => import('@/components/skeletons/listagem/produtos.vue'),
    menuLateral: () => import('@/components/skeletons/listagem/menu-lateral.vue'),
    pitchbar: () => import('@/components/skeletons/geral/pitchbar.vue')
  }
}
</script>

<style lang="css" scoped>
</style>
