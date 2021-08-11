<template>
    <section class="produtosHome">
        <div class="container">
            <br>
            <br>
            <div class="titleSection text-center">
                <h1>ESCOLHA SEU TRATAMENTO</h1>
                <p>Recomendamos o uso mínimo de 3 potes para um melhor resultado</p>
            </div>
            <br>
            <br>
            <div class="row">

                 <div class="col-sm-4 tirarMargin" style="margin-top:50px;">
                    <div class="col-sm-12 blocksProd">
                    <div style="padding-left: 35px;">
                        <div style="margin-left: -20px;">
                        <div style="font-size: 17px; margin-left: -36px; margin-right: -20px; margin-top:-20px; background:#f8f8f8!important; padding-bottom:0px; padding-top:0px;">
                            <div class="descontoProd" style="margin-left: 0px;">19%<br>OFF</div>
                            <div class="tituloProd"><span>COMPRE 1</span><br><font style="color:#888; font-size:13px;">1 mês de tratamento</font></div>
                        </div>
                        </div>
                    </div>
                    <div class="col-sm-12" style="text-align:center; padding:0px 0px 0px 0px;">
                        <img class="imgresponsive" src="@/assets/img/1-pote.jpg">
                    </div>

                    <div>
                        <p style="font-size:12px;"><b>Contém:</b><font style="color:#888;"> 1 pote New Hair Caps com 30 cápsulas cada</font></p>
                    </div>
                    <div style="font-size:13px; padding-top:10px; border-top:1px solid #ddd;"></div>
                    <div class="col-sm-12" style="line-height:30px; width:100%; text-align:center; margin-top:10px;">                   
                        <p style="font-size:20px; margin-top: 10px; color:#888;"><s>De: R$119,90</s></p>
                        <p style="font-size:20px; color:#888;">Por apenas: <span style="color: #000; font-weight:bold;font-size:20px;">R$97,70</span></p>
                        <p style="margin-top:-10px;"><img class="imgoU" src="@/assets/img/img-ou.png"></p>
                        <p style="color:#000; font-size:20px;">12x sem juros de</p>
                        <p style="color:#000; font-size:45px;font-weight: 700; padding-top:2px;"><span>R$ 8,14</span><span class='textSemJuros' style="font-size:14px; font-weight:bold;"></span></p>      
                        <input type="submit" value="COMPRE AGORA" class="btnComprar" @click="addCartBoxCompra()">                      
                    </div> 
                    <div class="col-sm-12"> 
                        <p align="center" style="margin-top:20px;"><img src="@/assets/img/ico-frete-gratis.png"></p>
                    </div>
                    </div>
                    <div style="position:absolute; top:27%;right:20%"><img class="imgresponsive2" src="@/assets/img/frete-gratis.png"></div>
                    <br class="mob"><br class="mob"><br class="desk"><br class="desk">
                </div>

                <div class="col-sm-4">
                    <div class="col-sm-12" style=" border: 1px solid #ddd; padding: 20px; box-shadow: 0px 10px 30px rgb(171 171 171 / 60%);">
                    <div style="padding-left: 35px;">
                        <div style="margin-left: -20px;">
                        <div style="font-size: 17px; margin-left: -35px; margin-right: -20px; margin-top:-20px; background:#FF03A8!important; padding-bottom:0px; padding-top:0px;">
                            <div class="descontoProd" style="margin-left: 0px; color:white;">37%<br>OFF</div>
                            <div class="tituloProd" style="color: #fff;"><span>PROMOÇÃO DE INVERNO</span><br><font style="color:#fff; font-size:13px;">COMPRE 3 GANHE BRINDE</font></div>

                            <div style="background-color:#ffea3b; color:#f13787; width:100%; padding: 10px; text-align: center;"><i class="fa fa-star"></i> <strong>KIT MAIS VENDIDO</strong>
                            <i class="fa fa-star"></i></div>

                        </div>
                        </div>
                    </div>
                    <div class="col-sm-12" style="text-align:center; padding:20px 0px 0px 0px;">
                        <img class="imgresponsive" src="@/assets/img/3-potes.jpg">
                        <p style="margin-top: -100px; padding: 0px 0px 0px 120px;"><img src="@/assets/img/mascara-FRETE.png"></p>
                    </div>
                    <div>
                        <p style="font-size:12px;"><b>Contém:</b><font style="color:#888;"> 3 potes New Hair Caps com 30 cápsulas cada</font></p>
                    </div>

                    <!--  <div style="font-size:13px; padding-top:10px; border-top:1px solid #ddd;"></div> -->
                    <div style="padding-left: 35px; margin-top:25px;">
                    <div style="margin-left: -20px;">
                        <div style="font-size: 17px; margin-left: -35px; margin-right: -20px; margin-top:-20px; background:#FF03A8 !important; padding-bottom:0px; padding-top:0px;">
                                <div class="row" style="text-align: center;">
                                    <div class="col-5 col-sm-5" style="text-align: right;">
                                    <div style="margin-top:5px;
                                    position: relative;
                                    bottom: -2px;
                                    ">
                                    <img src="@/assets/img/relogio.png"></div>
                                    </div>
                                    <div class="col-7 col-sm-7" style="text-align: left; margin-left: -20px; margin-top: 5px;">
                                        <span class="center" style="font-size:14px; color:#fff; font-weight: bold;">OFERTA EXPIRA EM:</span>
                                        <p id="crono" style="
                                        margin-top: -10px;
                                        font-weight: bold;
                                        font-size: 34px;
                                        color: rgb(255, 255, 255);
                                        margin-bottom: -7px;
                                        " ></p>
                                </div>
                                </div>
                            </div>
                        </div>
                        </div>
                    <div class="col-sm-12" style="line-height:30px; width:100%; text-align:center; margin-top:10px;">                   
                        <p style="font-size:20px; margin-top: 20px; color:#888;"><s>De: R$359,70</s></p>
                        <p style="font-size:20px; color:#888;">Por apenas: <span style="color: #000; font-weight:bold;font-size:20px;">R$227,70</span></p>
                        <p style="margin-top:-10px;"><img class="imgoU" src="@/assets/img/img-ou.png"></p>
                        <p style="color:#000; font-size:20px;">12x sem juros de</p>
                        <p style="color:#000; font-size:45px;font-weight: 700;"><span>R$ 18,97</span><span class='textSemJuros' style="font-size:14px; font-weight:bold;"></span></p>
                        <input type="submit" value="COMPRE AGORA" style="background-color:#ff03a8;" class="btnComprar" @click="addCartBoxCompra1()">                                    
                    </div>
                    <div class="col-sm-12"> 
                        <p align="center" style="margin-top:20px;"><img src="@/assets/img/ico-frete-gratis.png"></p>
                    </div>
                    </div>
                    <div style="display: none; position:absolute; top:110px; left:45px; z-index:9;"><img class="imgresponsive2" src="@/assets/img/frete-gratiss.png"></div>
                    <br class="mob"><br class="mob"><br class="desk"><br class="desk">
                </div>



                <!-- ========BLOCO 3===============-->
                <div class="col-sm-4 tirarMargin" style="margin-top:50px;">
                    <div class="col-sm-12 blocksProd">
                    <div style="padding-left: 35px;">
                        <div style="margin-left: -20px;">
                        <div style="font-size: 17px; margin-left: -36px; margin-right: -20px; margin-top:-20px; background:#f8f8f8!important; padding-bottom:0px; padding-top:0px;">
                            <div class="descontoProd" style="margin-left: 0px; background: #42C7A1 !important;">54%<br>OFF</div>
                            <div class="tituloProd"><span>COMPRE 6</span><br><font style="color:#888; font-size:13px;">6 meses de tratamento</font></div>
                        </div>
                        </div>
                    </div>
                    <div class="col-sm-12" style="text-align:center; padding:20px 0px 0px 0px;">
                        <img class="imgresponsive" src="@/assets/img/newhairfrasco6.jpg">
                        <p style="margin-top: -100px; padding: 0px 0px 0px 120px;"><img src="@/assets/img/mascara-FRETE.png"></p>
                    </div>
                    <div>
                        <p style="font-size:12px;"><b>Contém:</b><font style="color:#888;"> 6 potes New Hair Caps com 30 cápsulas cada</font></p>
                    </div>
                    <div style="font-size:13px; padding-top:10px; border-top:1px solid #ddd;"></div>
                        <div class="col-sm-12" style="line-height:30px; width:100%; text-align:center; margin-top:10px;">                   
                        <p style="font-size:20px; margin-top: 10px; color:#888;"><s>De: R$714,00</s></p>
                        <p style="font-size:20px; color:#888;">Por apenas: <span style="color: #000; font-weight:bold;font-size:20px;">R$327,70</span></p>
                        <p style="margin-top:-10px;"><img class="imgoU" src="@/assets/img/img-ou.png"></p>
                        <p style="color:#000; font-size:20px;">12x sem juros de</p>
                        <p style="color:#000; font-size:45px;font-weight: 700;"><span>R$ 27,31</span><span class='textSemJuros' style="font-size:14px; font-weight:bold;"></span></p>
                        <input type="submit" value="COMPRE AGORA" class="btnComprar" @click="addCartBoxCompra2()">                                
                    </div>
                  
                    <div class="col-sm-12"> 
                        <p align="center" style="margin-top:20px;"><img src="@/assets/img/ico-frete-gratis.png"></p>
                    </div>
                    </div>
                    <div style="display: none; position:absolute; top:110px; left:45px; z-index:9;"><img class="imgresponsive2" src="@/assets/img/frete-gratiss.png"></div>
                    <br class="mob"><br class="mob"><br class="desk"><br class="desk">
                </div>
            </div><!--ROW-->
        </div><!--container-->
    </section>
</template>

<script>
import Comunicacao from '@/comunicacao.js'
export default {
    mounted(){
        // CRONOMETRO
        // Set the date we're counting down to
        var countDownDate = new Date("jan 29, 2022 23:59:59").getTime();
        // Update the count down every 1 second
        var x = setInterval(function() {
        // Get today's date and time
        var now = new Date().getTime();
        // Find the distance between now and the count down date
        var distance = countDownDate - now;
        // Time calculations for days, hours, minutes and seconds
        var days = Math.floor(distance / (1000 * 60 * 60 * 24));
        var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        var seconds = Math.floor((distance % (1000 * 60)) / 1000);
        var daybr = days;
        console.log(daybr);
        const textoHoras = (`00${hours}`).slice(-2);
        const textoMinutos = (`00${minutes}`).slice(-2);
        const textosegundos = (`00${seconds}`).slice(-2);

        // Display the result in the element with id="demo"
        document.getElementById("crono").innerHTML = textoHoras + ":"
        + textoMinutos + ":" + textosegundos;

        // document.getElementById("crono1").innerHTML = textoHoras + ":"
        // + textoMinutos + ":" + textosegundos;

        // document.getElementById("crono2").innerHTML = textoHoras + ":"
        // + textoMinutos + ":" + textosegundos;

        // If the count down is finished, write some text
        if (distance < 0) {
            clearInterval(x);
            document.getElementById("demo").innerHTML = "EXPIRED";
        }
        }, 1000);
        // CRONOMETRO
    },
     data(){ 
        return {
        boxCompraCarrinho: {
        tipo: "produto",
        itens: [
        {
            idProduto: "28",
            idAtributoSimples: "0",
            idUnidadeVenda: "0",
            idArmazem: "0",
            quantidade: "1",
            adicional: "",
            parametros: ""
        }
        ]
        },
        boxCompraCarrinho1: {
        tipo: "produto",
        itens: [
        {
            idProduto: "29",
            idAtributoSimples: "0",
            idUnidadeVenda: "0",
            idArmazem: "0",
            quantidade: "1",
            adicional: "",
            parametros: ""
        },
        ]
        },
        boxCompraCarrinho2: {
        tipo: "produto",
        itens: [
        {
        idProduto: "30",
        idAtributoSimples: "0",
        idUnidadeVenda: "0",
        idArmazem: "0",
        quantidade: "1",
        adicional: "",
        parametros: ""
        }
        ]
        },
    }
    },
    components:{

    },
    methods: {
    addCartBoxCompra() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra1() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho1;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho1.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    addCartBoxCompra2() {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = this.boxCompraCarrinho2;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {
          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho2.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    },
    }
}
</script>

<style lang="scss" scoped>
.produtosHome{
    .titleSection{
        h1{
          font-size:36px;
          font-weight: 500;  
          color:#404040;
        }
        P{
           color:#888;
           font-size:15px; 
        }
    }
}
// Blocos PROD NuVEM
.novi-backdrop, .novi-overlay {
background: rgba(255, 255, 255, 0.5) !important;
}
.btnComprar{
    background-color:#04b900;
    color:#fff;
    font-weight: bold;
    width:200px;
    height:60px;
    border-radius:6px;
    font-family: 'Helvetica',sans-serif;
    border:none;
    cursor: pointer;
    transition: 0.4s ease;
}
.btnComprar:hover{
    opacity: 0.8;
}

/* ############ BOTÃO COMPRAR ########### */ 
.blocksProd {
background: #fff;
border: 1px solid #ddd;
padding: 20px;
box-shadow: 0px 10px 30px rgb(171 171 171 / 60%);

}

.descontoProd {
display: inline-block;
padding: 15px 15px 15px 15px;
font-weight: bold;
font-size: 17px;
line-height: 17px;
color: #fff;
background-color: #42C7A1;
}


.tituloProd {
display: inline-block;
margin-left: 10px;
font-size: 11px;
}

.tituloProd span {
font-size: 16px;
font-weight: 900;
}

@media (max-width: 580px) {
input.btnComprar {
font-size: 12px !important;
}
.imgresponsive{
width: 100%;
}
.imgresponsive2{
width: 80%;
}

.tirarMargin{
margin-top: 0px !important;
}
}
@media screen and (max-width: 800px){
input.btnComprar{
font-size: 14px !important;
width: 220px !important;
height: 60px;
}
}


/*////////////////VIDEO/////////////*/
.grtvideo-popup-content {
margin-top: 100px !important;
}

#player{
background: orange;
}

.cirulo {
font-weight: bold;
padding: 10px 10px 9px 10px;
border-radius: 50%;
background: orange;
animation: 1.5s linear 0s infinite normal pulse;
}

@keyframes pulse {
0% {
/* transform: scale(0.9);*/
box-shadow: 0px 1px 0px 3px transparent, 0px 0px 0px 0px #efeb2450;
}
30% {
box-shadow: 0px 1px 0px 3px transparent, 0px 0px 0px 5px #efeb2450;
}
70% {
box-shadow: 0px 1px 0px 3px transparent, 0px 0px 0px 15px #efeb2410;
}
100% {
transform: scale(1);
box-shadow: 1px 1px 3px 1px transparent, 0px 0px 0px 20px transparent;
}
}
</style>