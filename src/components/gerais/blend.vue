<template>
    <section class="blend">
        <div class="container">
            <div class="titleSection text-center">
                <h1 style="font-family: 'Poppins',sans-serif !important;margin-bottom:0px;">O BLEND DE VITAMINAS MAIS PODEROSO</h1>
                <p style=" font-family: 'Poppins',sans-serif !important;margin-top:-10px;">AGORA TAMBÉM EM GOMAS</p>
            </div>

            <div class="row deskf" style="position:relative;right:-3%;" id="acertaBlend">
                <div class="col-sm-4" style="position:relative;">
                    <img src="@/assets/img/gummies_frasco.png" width="400px" style="position:absolute;" alt="">
                </div>
                <div class="col-sm-4 d-flex colP justify-content-center" style="margin-top:80px;margin-bottom:40px;margin-left:-30px;">
                    <div class="col-6">
                        <p>
                            REDUZ A QUEDA <br>
                            <strong>EM ATÉ 96%</strong>
                        </p>
                        <p>
                            NÃO ENGORDA<br>
                            <strong>ZERO AÇUCAR</strong>
                        </p>
                        <p>
                            CRESCIMENTO <br>
                            <strong>ACELERADO</strong>
                        </p>
                        <p>
                            FÓRMULA <br>
                            <strong>NATURAL</strong>
                        </p>
                        <p>
                            PARA CABELOS<br>
                            <strong>E UNHAS</strong>
                        </p>
                    </div>
                    <div class="col-2 text-center colCheck">
                        <img src="@/assets/img/check_icon.png" class="check_icon" alt="">
                        <img src="@/assets/img/check_icon.png" class="check_icon" alt="">
                        <img src="@/assets/img/check_icon.png" class="check_icon" alt="">
                        <img src="@/assets/img/check_icon.png" class="check_icon" alt="">
                        <img src="@/assets/img/check_icon.png" class="check_icon" alt="">
                    </div>
                    <div class="col-6">
                         <p style="text-align:left">
                            REDUZ A QUEDA <br>
                            <strong>EM ATÉ 96%</strong>
                        </p>
                        <p style="text-align:left">
                            NÃO ENGORDA<br>
                            <strong>ZERO AÇUCAR</strong>
                        </p>
                        <p style="text-align:left">
                            CRESCIMENTO <br>
                            <strong>ACELERADO</strong>
                        </p>
                        <p style="text-align:left">
                            FÓRMULA <br>
                            <strong>NATURAL</strong>
                        </p>
                        <p style="text-align:left">
                            PARA CABELOS<br>
                            <strong>E UNHAS</strong>
                        </p>
                    </div>
                </div>
                <div class="col-sm-4">
                    <img src="@/assets/img/caps_frasco2.png" width="400px"  style="position:absolute;top:20px;left:-43px;" alt="">
                </div>
            </div>
             <img src="@/assets/img/gummiesmob.jpg" class="mob" style="width:100%;margin:50px 0px;" alt="">
            <div class="row">
                <router-link v-if="$route.path != '/produtos'" class="facaSeuPedido" to="/produtos">FAÇA SEU PEDIDO</router-link>
            </div>
        </div>
       
    </section>
</template>


<style lang="scss" scoped>
.blend{
    padding:40px 0px;
    margin:40px 0px 80px 0px;
    .check_icon{
        margin:10px 0px;
        max-width: 100%;
    }
    .mx100{
        max-width: 100%;
    }
    .colP .col-6{
        p{
            text-align:right;
            margin:10px 0px;
            font-family: 'Roboto', sans-serif;
            line-height:18px;
            color:#676767;
            font-size:18px;
            font-weight:300;
            strong{
                font-weight:bold !important;
            }
        }
    }
    .titleSection{
        margin-bottom:-20px;
        h1{
            color:#404040; 
            font-weight: 800;  
            font-size:36px;
        }
        p{
        color: #FFF;
        -webkit-text-stroke-width: 1px;
        -webkit-text-stroke-color: #000;
        font-size:36px;
        font-weight:800;
        }
    }
}
@media screen and (max-width: 768px){
    .blend{
        margin: 40px 0px 20px 0px;
        .titleSection{
            h1{
                font-size:28px;
            }
            p{
                font-size:23px;
            }
        }
    }
}
</style>