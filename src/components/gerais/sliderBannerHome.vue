<template>
    <section class="slideHome">
        <a href="/produtos">
            <flickity class="flickity" ref="flickity" :options="flickityOptions" style="cursor: pointer;">
                <div class="carousel-cell">
                        <img src="@/assets/img/new-hair-gummies-lancamento-banner-principal-homepage-agosto-2021.jpg" alt="">
                </div>
                <div class="carousel-cell">
                        <img src="@/assets/img/New-Hair-Desktop-Home---Beauty-Festival-Inverno.png" alt="">
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
.a{
    cursor: pointer;
}
.slideHome{
    .flickity{  
        .flickity-viewport{
            cursor:pointer !important;
        }
        .carousel-cell{
            img{
                min-height:674px !important;
                width: 1920px !important;
                margin:0 auto !important;
                display:block;
                align-content: center;
                
            }
        }
        .carousel-cell2{
            display: none;
        }
    }
}
@media screen and ( max-width: 768px ) {
    .carousel-cell {
        display: none;    
    }
}
</style>