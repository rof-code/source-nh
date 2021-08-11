<template>
    <section class="caps">
        <div class="container">
            <div class="row gomasRow deskf">
                <div class="col-sm-7 col7">
                    <h1 style="color:#fff;font-family:'Poppins',sans-serif;font-weight:800;">AS CÁPSULAS MAIS FAMOSAS <br>
                    DO BRASIL, USADAS PELAS <br>
                    <span
                    style="
                    color: transparent;
                    -webkit-text-stroke-width: 0.5px;
                    -webkit-text-stroke-color: #fff;
                    ">
                    MAIORES CELEBRIDADES</span></h1>
                    <p style="margin-top:30px;">
                        Prático e poderoso. Esse é o nosso blend vitamínico na versão em  <br>
                        cápsulas da New Hair. Composta por 17 vitaminas que vão <br>
                        estimular o crescimento e reduzir a queda dos seus fios.
                    </p>
                    <div class="row  colGoma">
                        <div class="col-sm-3">
                            <img class="ico_goma" src="@/assets/img/icon_caps.png" alt="">
                            <p>RÁPIDA<br>
                            <strong>ABSORÇÃO</strong></p>
                        </div>
                        <div class="col-sm-3">
                            <img class="ico_goma"  src="@/assets/img/icon_gelo.png" alt="">
                            <p>NÃO<br>
                            <strong>ENGORDA</strong></p>
                        </div>
                        <div class="col-sm-3">
                            <img class="ico_goma"  src="@/assets/img/icon_trigo.png" alt="">
                            <p>NÃO CONTÉM<br>
                            <strong>GLÚTEN</strong></p>
                        </div>
                        <div class="col-sm-3">
                            <img  class="ico_goma" src="@/assets/img/icon_sal.png" alt="">
                            <p>ZERO<br>
                            <strong>SÓDIO</strong></p>
                        </div>
                    </div>
                    <div class="acertaBotao" style="display:flex;justify-content:flex-end;justify-items:end;justify-self:end;">
                        <a href="/produtos" style="margin:40px 0px 0px 0px;display:flex;" class="facaSeuPedido">FAÇA SEU PEDIDO</a>
                    </div>
                </div>
                <div class="col-sm-5">
                    <img class="poteAbs" src="@/assets/img/new-hair-caps-frasco-sessao-sobre-produto.png" style="max-width:90%" alt="">
                    <div class="ingredientes">
                        <div class="tituloI text-center">
                            <h4>Nº 1</h4>
                            <p>NO ASSUNTO <br>
                            SAÚDE CAPILAR</p>
                        </div>
                        <div class="pI">
                            <p>
                                Vitaminas A, B1, B2, B3, <br>
                                B5, B6, B7, B9, B12, C, <br>
                                D3, E, Cromo picolinato, <br>
                                Cobre, Ferro, Selênio e <br>
                                Zinco.
                            </p>
                        </div>
                    </div>
                </div>
            </div><!--first--row-->
        </div>
        <div class="mobCaps mob">
                <img src="@/assets/img/N2.png"  style="max-width:100%;margin-top:-90px;"  alt="">
                <div class="container">
                    <h1 style="color:#fff;margin:30px 0px;">AS CÁPSULAS MAIS <br>
                    FAMOSAS DO BRASIL, <br>
                    USADA PELAS <br>
                    <span style="color: transparent;-webkit-text-stroke-width: 0.5px;-webkit-text-stroke-color: #fff;font-size: 27px">MAIORES CELEBRIDADES</span></h1>
                    <p style="color:#fff;font-family:'Roboto',sans-serif;font-size:14px;font-weight:300;">
                        Prático e poderoso. Esse é o nosso blend vitamínico <br >
                        a versão em cápsulas da New Hair. Composta por <br>
                        17 vitaminas que vão estimular o crescimento e  <br>
                        reduzir a queda dos seus fios. <br>
                    </p>
                </div>
            </div>
            <beneficiosCaps />

    </section>
</template>

<script>

export default {
  components: {
    beneficiosCaps: () => import('@/components/gerais/beneficios-caps.vue')
  },
  data(){
    return {
      banners: [],
      bannerMeio: null,
      marcas: false,
      vitrineData: false,
      loading: {
        geral: true,
        banner: true
      },
      answer: [],
      answerOpened: null
    }
  },
  created(){
  }
}

</script>  

<style lang="scss" scoped>
.mobCaps{
    padding-top: 25px;
}
.caps{
.tituloI{
    background-color:#fd1a6d;
    width: 70%;
    h4{
        color:#fff;
        font-family:'Poppins',sans-serif;
        font-size:100px;
        letter-spacing: -5px;
        font-weight:800;
        width: 70%;
        position: relative;
        right:-20%;
    }
    p{
        position:relative;
        margin-top: 10px;
        right:-7%;
        top:-20px;
    }
}
.pI{
    p{
        font-family:'Roboto', sans-serif;
        color:#fff;
        background-color:#fd1a6d83;
        padding:20px 20px 20px 50px;
        font-size:15px;
        line-height:15px;
        width:100%;
        font-weight:lighter;
    }
}
.col7{
    text-align: right;
}

    .poteAbs{
        position: absolute;
        top: -62px;
        left: -130px;
    }
    .colGoma{
        margin-top:30px;
        position:relative;
        right:-3%;
        .col-sm-3{
            padding:0;  
            
            text-align: center;        
        }
       
    }
   
    .row{
        .col-sm-7{
            padding-right:50px;
            padding-left: 0px;
            p{
                font-family: 'Roboto',sans-serif;
                font-weight: lighter;
                color:#fff;
                line-height:25px;
                font-size:18px;
                margin-top:7px;
            }
        }
        .col-sm-5{
            position:relative;
            right: -5%;
        }
    }
    background-color:#ff2c7b;
    padding:40px 0px;
    .ingredientes{
        margin-top:100px;
        padding:5px 50px 0px 25px;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        align-self: flex-end;
        align-content: flex-end;
        align-items: flex-end;
        p{
            color:#fff;
            font-family: 'Poppins',sans-serif;
        }
    }
}
</style>