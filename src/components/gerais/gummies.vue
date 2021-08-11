<template>
    <section class="gummies">
        <div class="container">
            <div class="row gomasRow deskf">
                <div class="col-sm-5">
                    <div class="ingredientes">
                        <div class="tituloI text-center" style="
                            background-color: rgb(71, 40, 86);
                            width: 70%;
                            padding-bottom:15px;
                            margin: 0px 40p;">
                            <h4 style="color:#fff;font-family:'Poppins',sans-serif;font-size:100px;font-weight:800;margin-bottom:-10px;margin-left:-6%;letter-spacing:-5px;">Nº 1</h4>
                            <p style="margin-left:-10%;">NO ASSUNTO <br>
                            SAÚDE CAPILAR</p>
                        </div>
                        <div class="pI">
                            <p style="font-family:'Roboto', sans-serif;color:#fff;background-color:#4b2c5a;padding:20px 0px 20px 40px;font-size:15px;line-height:15px;width:70%;font-weight:lighter;">Vitaminas A, B1, B2, B3,<br>
                            B5, B6, B7, B9, B12, C, <br>
                            D3, E, Cromo picolinato, <br>
                            Selênio e Zinco.</p>
                        </div>
                       
                        <img class="poteAbs" src="@/assets/img/new-hai-gummies-frasco-sessao-sobre-produto.png" style="max-width:100%;" alt="">
                    </div>
                </div>
                <div class="col-sm-7 col7">
                    <h1 style="color:#fff;font-family:'Poppins',sans-serif;font-weight:800;">NOVO NEW HAIR GUMMIES, <br>
                    COM SABOR SURPREENDENTE <br>
                    <span
                    style="color: transparent;
                    -webkit-text-stroke-width: 0.5px;
                    -webkit-text-stroke-color: #fff;"
                    >DE MORANGO <img src="@/assets/img/morango.png" style="max-width:100%;margi-top:-5px;" alt=""></span>
                    </h1>
                    <p style="margin-top:30px;">Os benefícios que você já conhece da New Hair, mas agora de uma <br>
                    maneira mais divertida de consumir. Nossa goma é zero açúcar, <br>
                    zero glúten e zero lactose. Apenas uma bala ao dia para você sentir a <br>
                    transformação dos seus fios de dentro para fora.</p>
                    <div class="row  colGoma">
                        <div class="col-sm-3">
                            <img class="ico_goma" src="@/assets/img/icon_urso.png" alt="">
                            <p>FÁCIL<br>
                            <strong>CONSUMO</strong></p>
                        </div>
                        <div class="col-sm-3">
                            <img class="ico_goma"  src="@/assets/img/icon_gelo.png" alt="">
                            <p>ZERO<br>
                            <strong>AÇUCAR</strong></p>
                        </div>
                        <div class="col-sm-3">
                            <img class="ico_goma"  src="@/assets/img/icon_trigo.png" alt="">
                            <p>NÃO CONTÉM<br>
                            <strong>GLUTÉN</strong></p>
                        </div>
                        <div class="col-sm-3">
                            <img  class="ico_goma" src="@/assets/img/icon_sal.png" alt="">
                            <p>ZERO<br>
                            <strong>SÓDIO</strong></p>
                        </div>
                    </div>
                    <a href="/produtos" style="margin:40px 0px 0px 0px" class="facaSeuPedido">FAÇA SEU PEDIDO</a>
                </div>
            </div><!--first--row-->

            <div class="mobGum mob">
                <img src="@/assets/img/N1.png"  style="max-width:100%;margin-top:-90px;"  alt="">
                <h1 style="color:#fff;margin:30px 0px;">NOVO NEW HAIR <br>
                GUMMIES, COM SABOR <br>
                SURPREENDENTE <br>
                <span style="color: transparent;-webkit-text-stroke-width: 0.5px;-webkit-text-stroke-color: #fff;font-size: 27px">DE MORANGO</span></h1>
                <p style="color:#fff;font-family:'Roboto',sans-serif;font-size:14px;font-weight:300;">
                    Os benefícios que você já conhece da New Hair, <br>
                    mas agora de uma maneira mais divertida de <br>
                    consumir. Nossa goma é zero açúcar, zero glúten e <br>
                    zero lactose. Apenas uma bala ao dia para você <br>
                    sentir a transformação dos seus fios de dentro para <br>
                    fora.
                </p>

                 <beneficiosGummies />

            </div>
        </div><!--container-->
    </section>
</template>

<script>

export default {
  components: {
    beneficiosGummies: () => import('@/components/gerais/beneficios-gummies.vue')
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
.gummies{
    .poteAbs{
        position: absolute;
        top: -159px;
        left: 135px;
    }
    .colGoma{
        margin-top:30px;
        position:relative;
        left:-3%;
        .col-sm-3{
            padding:0;  
            
            text-align: center;        
        }
       
    }
   
    .row{
        .col-sm-7{
            padding-left:50px;
            padding-right: 0px;
            p{
                font-family: 'Roboto',sans-serif;
                font-weight: lighter;
                color:#fff;
                line-height:25px;
                font-size:18px;
                margin-top:7px;
            }
        }
    }
    background-color:#4f305e;
    padding:40px 0px;
    .ingredientes{
        margin-top:100px;
        padding:5px 50px 0px 25px;
        p{
            color:#fff;
            font-family: 'Poppins',sans-serif;
        }
    }
}
</style>