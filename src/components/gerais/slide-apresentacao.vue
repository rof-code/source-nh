<template>
    <section class="apresentacao" style="max-width:100% !important;">
        <div class="row desk" style="max-width:100% !important;">
            <img  src="@/assets/img/01-min.jpg">
            <img  src="@/assets/img/02-min.jpg">
            <img  src="@/assets/img/03-min.jpg">
            <img  src="@/assets/img/04-min.png">
            <img  src="@/assets/img/05-min.jpg">
            <img  src="@/assets/img/06-min.jpg">
            <img  src="@/assets/img/07-min.jpg">
            <img  src="@/assets/img/08-min.jpg">
            <img  src="@/assets/img/09-min.jpg">
            <img  src="@/assets/img/10-min.jpg">
            <img  src="@/assets/img/11-min.jpg">
            <img  src="@/assets/img/12-min.jpg">
            <img  src="@/assets/img/13-min.jpg">
            <img  src="@/assets/img/14-min.jpg">
            <img  src="@/assets/img/15-min.jpg">
            <img  src="@/assets/img/16-min.jpg">
            <img  src="@/assets/img/17-min.jpg">
            <img  style="margin-bottom:-10px;" src="@/assets/img/18-min.jpg">
        </div><!--row-->


        <div class="row mob">
            <img class="imgMobA" src="@/assets/img/01-min.jpg">
            <img class="imgMobA" src="@/assets/img/02-min.jpg">
            <img class="imgMobA" src="@/assets/img/03-min.jpg">
            <img class="imgMobA" src="@/assets/img/04-min.png">
            <img class="imgMobA" src="@/assets/img/05-min.jpg">
            <img class="imgMobA" src="@/assets/img/06-min.jpg">
            <img class="imgMobA" src="@/assets/img/07-min.jpg">
            <img class="imgMobA" src="@/assets/img/08-min.jpg">
            <img class="imgMobA" src="@/assets/img/09-min.jpg">
            <img class="imgMobA" src="@/assets/img/10-min.jpg">
            <img class="imgMobA" src="@/assets/img/11-min.jpg">
            <img class="imgMobA" src="@/assets/img/12-min.jpg">
            <img class="imgMobA" src="@/assets/img/13-min.jpg">
            <img class="imgMobA" src="@/assets/img/14-min.jpg">
            <img class="imgMobA" src="@/assets/img/15-min.jpg">
            <img class="imgMobA" src="@/assets/img/16-min.jpg">
            <img class="imgMobA" src="@/assets/img/17-min.jpg">
            <img class="imgMobA" style="margin-bottom:-10px;" src="@/assets/img/18-min.jpg">
        </div><!--row-->
    </section>
</template>

<script>
export default {
    name: 'SlideApresentacao'
}
</script>

<style scoped>
.desk{display:block;}
.mob{display: none;}

@media screen and (max-width:768px){
    .desk{display: none;}
    .mob{display:block;}
}
</style>