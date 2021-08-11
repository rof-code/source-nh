<template>
    <section class="slide">
        <a href="/produtos">
        <flickity class="flickity" ref="flickity" :options="flickityOptions">
            <div class="carousel-cell">
                <img src="@/assets/img/new-hair-gummies-banner-lancamento-home-mobile-agosto-2021.jpg" alt="">    
            </div>
            <div class="carousel-cell">
                <img src="@/assets/img/New-Hair-Home-Mobile---Beauty-Festival-Inverno.png" alt="">
            </div>
        </flickity>
        </a>
    </section>
</template>
<script>
import flickity from 'vue-flickity';
export default {
    components:{
        flickity
    },
    data(){
        return{
            flickityOptions:{
                wrapAround: true,
                freeScroll: true,
                groupCells: true,
                autoPlay: 5000,
                prevNextButtons: false,
                pageDots:false,
            }
        }
    },     
}
</script>
<style lang="scss" scoped>

.slide{
    .flickity{ 
        .carousel-cell{
            width:100% !important;
            img{
                min-width: 100% !important;
                min-height:867px !important;
            }
        }
    }
}
</style>