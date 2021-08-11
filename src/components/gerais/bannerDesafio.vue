<template>
    <section class="bannerDesafio">
        <div class="bannerDesk desk">
        </div>

        <div class="bannerMob mob" style="width:100%">
            <img src="@/assets/img/bannerDesafioMob.jpg" width="100%" alt="">
        </div>
    </section>
</template>

<style lang="scss" scoped>
.desk{
    display:block !important;
}
.mob{display:none !important;}

.bannerDesk.desk{
    background-image: url('../../assets/img/bannerDesafio.jpg');
    background-size:1920px;
    background-position:center;
    background-repeat:no-repeat;
    height:450px;
    display: block;
    margin:0 auto;
}
@media screen and(max-width:768px){
   .desk{
    display:none !important;
    }
    .mob{display:block !important;} 
    }
</style>