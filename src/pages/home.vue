<template>
  <main>
    <menuMob/>
    <menuNH/>
    <ExitPop/>
    <transition name="fade">
      <sklGeral v-if="loading.geral" />
    </transition>

    <transition name="fade">
      <div v-if="!loading.geral">

        <transition name="fade">
          <sklBanner v-if="loading.banner" />
        </transition>
          <div class="hiddenDesk">
            <sliderBannerHome/>
          </div>
          
          <div class="hiddenMob">
            <sliderMob/>
          </div>
          
       
        <div class="hiddenMob">
     
        </div>
        <pitchbar class="pitchbarHome" />

        <famososRecomendam />


        <!-- <section id="beneficios">
          <div class="container">
            <div class="row">
              <div class="col-12">
                <h2 class="beneficios-t1">CONHEÇA ALGUNS BENEFÍCIOS</h2>
                <p class="beneficios-t2">
                  Composição rica em vitaminas, antioxidantes e aminoácidos essenciais.
                </p>
              </div>
            </div>

            <div class="row">
              <div class="col-sm-12 col-md-3 beneficios-item">
                <div class="beneficios-imgContainer">
                  <img src="@/assets/img/home/beneficios/01.png" alt="">
                </div>
                <h3 class="beneficios-t3">
                  Diminui a queda <br v-if="screenWidth >= 1024">em até 96%
                </h3>
                <p class="beneficios-text">
                  Reduz a queda capilar <br v-if="screenWidth >= 1024">proporcionando um volume incrível e com aspecto mais saudável, além de eliminar pontas duplas.
                </p>
              </div>
              <div class="col-sm-12 col-md-3 beneficios-item">
                <div class="beneficios-imgContainer">
                  <img src="@/assets/img/home/beneficios/02.png" alt="">
                </div>
                <h3 class="beneficios-t3">
                  Crescimento <br v-if="screenWidth >= 1024">Acelerado
                </h3>
                <p class="beneficios-text">
                  New Hair pode fazer com que o <br v-if="screenWidth >= 1024">seu cabelo cresça até 6x mais rápido, de forma saudável, podendo chegar em até 4cm ao mês.
                </p>
              </div>
              <div class="col-sm-12 col-md-3 beneficios-item">
                <div class="beneficios-imgContainer">
                  <img src="@/assets/img/home/beneficios/03.png" alt="">
                </div>
                <h3 class="beneficios-t3">
                  Fortalecimento <br v-if="screenWidth >= 1024">das unhas
                </h3>
                <p class="beneficios-text">
                  Fortalece as unhas, deixando-as mais <br v-if="screenWidth >= 1024">resistentes à quebra, como também promove o crescimento.
                </p>
              </div>
              <div class="col-sm-12 col-md-3 beneficios-item">
                <div class="beneficios-imgContainer">
                  <img src="@/assets/img/home/beneficios/04.png" alt="">
                </div>
                <h3 class="beneficios-t3">
                  Cabelo com mais <br v-if="screenWidth >= 1024">brilho e maciez
                </h3>
                <p class="beneficios-text">
                  As vitaminas estimulam a produção <br v-if="screenWidth >= 1024">do lipídio que recupera e traz vida ao cabelo. Ou seja: ação hidratante.
                </p>
              </div>
              <div class="col-12">
                <router-link class="facaSeuPedido beneficiosBtComprar" to="/produtos">FAÇA SEU PEDIDO</router-link>
              </div>
            </div>
          </div>
        </section> -->
        <blend/>
        <gummies/>
        <caps/>
        <produtosEscolha/>
       

        <!-- <section id="bannerMeio" class="bannerDefault" v-if="bannerMeio">
          <router-link to="/produtos" class="bannerMeio-link">
            <img :src="bannerMeio[0].dimensoes[screenWidth < 770 ? 'mobile' : 'desktop'][tipoImg.banner]" alt="">
          </router-link>
        </section> -->
        <bannerDesafio/>
        <comentarios/>
        <!-- <section id="midia">
          <div class="container">
            <div class="row">
              <div class="col-12">
                <h1 class="midia-t1" >NOSSAS VITAMINAS <br v-if="screenWidth <= 767"> NA MÍDIA</h1>
                <p class="midia-t2">Veja o que dizem sobre nossas vitaminas<br v-if="screenWidth <= 767"> nos maiores meios de comunicação do País.</p>
              </div>
              <div class="col-sm-12 col-md-3 text-center">
                <img class="midia-img" src="@/assets/img/home/midia/01.jpg">
                <p class="midia-text">“Uma mudança real em pouco tempo. A tecnologia, em cápsulas, alcançou resultados expressivos em pouco tempo. Toda mulher precisa descobrir isso”</p>
              </div>

              <div class="col-sm-12 col-md-3 text-center">
                <img class="midia-img" src="@/assets/img/home/midia/02.jpg">
                <p class="midia-text">“Algumas vitaminas participam da regeneração dos fios, previnem queda e a quebra e outras fortalecem o cabelo desde a raiz, já que favorecem a circulação no couro cabeludo, beneficiando o crescimento saudável dos cabelos”</p>
              </div>

              <div class="col-sm-12 col-md-3 text-center">
                <img class="midia-img" src="@/assets/img/home/midia/03.jpg">
                <p class="midia-text">“Uma mulher começa pelos cabelos; os cabelos começam com esse tratamento que ajuda em praticamente tudo. É o melhor amigo dos fios, trata de dentro para fora”</p>
              </div>

              <div class="col-sm-12 col-md-3 text-center">
                <img class="midia-img" src="@/assets/img/home/midia/04.jpg"><br><br>
                <p class="midia-text">“Vitamina C e E, por exemplo, fazem parte desta lista e podem ser ainda mais poderosos que os cosméticos direcionados aos cuidados com cabelo e pele”</p>
              </div>


              <div class="col-12">
                <router-link class="facaSeuPedido beneficiosBtComprar" to="/produtos">FAÇA SEU PEDIDO</router-link>
              </div>
            </div>
          </div>
        </section> -->

        <!-- <section id="seguranca">
          <div class="container">
            <div class="row">
              <div class="col-12">
                <h2 class="seguranca-t1">
                  <span>AQUI SUA<br v-if="screenWidth <= 767"> COMPRA É 100% SEGURA</span>
                </h2>
                <p class="seguranca-t2">
                  Não se preocupe, comprar em nosso site<br v-if="screenWidth <= 767"> é seguro e totalmente confiável
                </p>
              </div>

              <div class="col-sm-12 col-md-3 text-center flex-container flex-dir-column align-middle">
                <div class="seguranca-img">
                  <img src="@/assets/img/home/seguranca/01.png">
                </div>
                <h3 class="seguranca-t3">DADOS<br>PESSOAIS</h3>
                <p class="seguranca-text">São totalmente sigilosos<br v-if="screenWidth <= 767"> e<br class="desk"> não são compartilhados.</p>
              </div>

              <div class="col-sm-12 col-md-3 text-center flex-container flex-dir-column align-middle">
                <div class="seguranca-img">
                  <img src="@/assets/img/home/seguranca/02.png">
                </div>
                <h3 class="seguranca-t3">SITE<br>CONFIÁVEL</h3>
                <p class="seguranca-text">Monitorado por empresas<br> de segurança digital.</p>
              </div>

              <div class="col-sm-12 col-md-3 text-center flex-container flex-dir-column align-middle">
                <div class="seguranca-img">
                  <img src="@/assets/img/home/seguranca/03.png">
                </div>
                <h3 class="seguranca-t3">DADOS<br>FINANCEIROS</h3>
                <p class="seguranca-text">Gravados em<br> ambiente 100% seguro.</p>
              </div>
              <div class="col-sm-12 col-md-3 text-center flex-container flex-dir-column align-middle">
                <div class="seguranca-img">
                  <img src="@/assets/img/home/seguranca/04.png">
                </div>
                <h3 class="seguranca-t3">ENTREGA<br>GRÁTIS</h3>
                <p class="seguranca-text">Logistica eficaz entregas<br>feitas no prazo combinado.</p>
              </div>

              <div class="col-12">
                <router-link class="facaSeuPedido beneficiosBtComprar" to="/produtos">FAÇA SEU PEDIDO</router-link>
              </div>
            </div>
          </div>
        </section> -->
        <compraSegura/>
        <section id="duvidas">
          <div class="container">
            <div class="row">
              <div class="col-12">
                <h2 class="duvidas-t1">AINDA TEM ALGUMA DÚVIDA?</h2>
                <p class="duvidas-t2">Caso ainda tenha alguma pergunta que não esteja aqui, fale com um de nossos atendentes!</p>
              </div>
              <div class="col-sm-12 col-md-6 columns">
                <div class="duvidas-item" v-for="(duvida, i) in faq.col1" :key="i">
                  <div class="duvidas-item-pergunta" @click="openAnswer(i)">
                    <h3>{{ duvida.pergunta }}</h3>
                    <i class="fa fa-caret-down" :class="{duvidasItemActive: answer[i] ? true : false}"></i>
                  </div>
                  <transition name="slideDown">
                    <div class="duvidas-item-resposta" v-if="answer[i]">
                      <p v-html="duvida.resposta"></p>
                    </div>
                  </transition>
                </div>
              </div>
              <div class="col-sm-12 col-md-6 columns">
                <div class="duvidas-item" v-for="(duvida, i) in faq.col2" :key="i">
                  <div class="duvidas-item-pergunta" @click="openAnswer(faq.col1.length+i)">
                    <h3>{{ duvida.pergunta }}</h3>
                    <i class="fa fa-caret-down" :class="{duvidasItemActive: answer[faq.col1.length+i] ? true : false}"></i>
                  </div>
                  <transition name="slideDown">
                    <div class="duvidas-item-resposta" v-if="answer[faq.col1.length+i]">
                      <p v-html="duvida.resposta"></p>
                    </div>
                  </transition>
                </div>
              </div>
              <div class="col-12">
                <router-link class="facaSeuPedido beneficiosBtComprar" to="/produtos">FAÇA SEU PEDIDO</router-link>
              </div>
            </div>
          </div>
        </section>

      </div>
    </transition>
  </main>
</template>

<script>
import comunicacao from '@/comunicacao.js'
import {mapState, mapGetters} from 'vuex'
import ExitPop from '@/components/gerais/ExitPop.vue';

export default {
  components: {
    menuNH: () => import('@/components/gerais/menuNH.vue'),
    menuMob: () => import('@/components/gerais/menuMob.vue'),
    sklGeral: () => import('@/components/skeletons/home.vue'),
    sklBanner: () => import('@/components/skeletons/home/banner.vue'),
    famososRecomendam: () => import('@/components/gerais/famosos-recomendam.vue'),
    sliderBannerHome: () => import('@/components/gerais/sliderBannerHome.vue'),
    sliderMob: () => import('@/components/gerais/sliderMob.vue'),
    blend: () => import('@/components/gerais/blend.vue'),
    compraSegura: () => import('@/components/gerais/compraSegura.vue'),
    bannerDesafio: () => import('@/components/gerais/bannerDesafio.vue'),
    gummies: () => import('@/components/gerais/gummies.vue'),
    comentarios: () => import('@/components/gerais/comentarios.vue'),
    caps: () => import('@/components/gerais/caps.vue'),
    produtosEscolha: () => import('@/components/gerais/produtosEscolha.vue'),
    pitchbar: () => import('@/components/gerais/pitchbar.vue'),
    ExitPop
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
  computed: {
    ...mapState({
      screenWidth: state => state.screenWidth,
      faq: state => state.duvidas.faq
    }),
    ...mapGetters(['tipoImg'])
  },
  methods: {
    openAnswer(index) {
      if (this.answerOpened != null) {
        this.$set(this.answer, this.answerOpened, false);
        if (index == this.answerOpened) {
          this.answerOpened = null;
          return;
        }
      }
      this.$set(this.answer, index, true);
      this.answerOpened = index;
    }
  },
  created(){
    this.$requestSend('get', '/v2/front/url/home', {}, (success, response) => {
      if (success){
        this.loading.geral = false;
        this.$aplicaSEO(response.data.estrutura);
        comunicacao.$emit('paginaCarregada', response.data);
      }
    });
    this.$requestSend('get', '/v2/front/showcase/banners/banner-principal', {}, (success, response) => {
      this.banners = success ? response.data.banners : false;
      this.loading.banner = false;
    });
    this.$requestSend('get', '/v2/front/showcase/products/escolha-tratamento', {}, (success, response) => {
      this.vitrineData = success ? response.data : false;
    });
    this.$requestSend('get', '/v2/front/showcase/banners/meio-home', {}, (success, response) => {
      this.bannerMeio = success ? response.data.banners : false;
    });
  }
}

</script>

<style>
  .home-t2,
  .home-t1{
    font-size: 36px;
    font-weight: 500;
    color: #404040;
    line-height: 1.11;
    text-align: center;
  }
  .home-t2{
    font-size: 20px;
  }
</style>

<style scoped>
  /* BENEFÍCIOS */
  #beneficios{
    background-color: #EDEDED;
    padding: 30px 0px 65px;
    margin-top: 45px;
  }
  .beneficios-t1{
    text-align: center;
    font-size: 36px;
    line-height: normal;
    font-weight: 500;
    color: #404040;
  }
  .beneficios-t2{
    text-align: center;
    font-size: 15px;
    line-height: 1.3;
    font-family: 'open sans', sans-serif;
    color: #888;
    margin-bottom: 40px;
  }
  .beneficios-t3{
    font-family: 'open sans', sans-serif;
    margin-top: 10px;
    color: #fc2aa8;
    font-weight: 700;
    font-size: 17px;
    margin-bottom: 17px;
  }
  .beneficios-item{
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  .beneficios-text{
    color: #666666;
    font-size: 13px;
    line-height: 1.5;
  }
  .beneficiosBtComprar{
    margin-top: 60px;
  }
  @media (max-width: 767px) {
    .beneficios-item:not(:last-child) .beneficios-text{
      margin-bottom: 13px;
    }
    .beneficiosBtComprar{
      margin-top: 43px;
    }
  }

  /* PITCHBAR */
  /* .pitchbarHome{
    margin-top: 20px;
  } */

  /* BANNER DO MEIO DA PÁGINA */
  @media (max-width: 767px) {
    .bannerMeio-link{
      width: 100%;
    }
  }


  /* MARCA NAS MIDIAS */
  #midia{
    margin-top: 45px;
  }
  .midia-t1{
    color: #404040;
    font-size: 36px;
    text-align: center;
    font-weight: 500;
    line-height: 1;
  }
  .midia-t2{
    color: #888;
    text-align: center;
    font-size: 15px;
    margin-top: 10px;
    margin-bottom: 45px;
  }

  .midia-img{
    margin-bottom: 20px;
  }
  .midia-text{
    font-size: 13px;
    line-height: 1.5;
    color: #666666;
  }
  @media (max-width: 767px) {
    .midia-img{
      margin-bottom: 15px;
    }
    .midia-text{
      margin-bottom: 13px;
    }
  }

  /* DUVIDAS FREQUENTES */
  #duvidas {
    margin-top: 45px;
    background-color:#ff2c7b;
    padding:30px 0px;
  }
  .duvidas-t1{
    font-size: 36px;
    font-weight: 500;
    line-height: 1;
    text-align: center;
    color: #fff;
  }
  .duvidas-t2{
    margin-top: 10px;
    font-size: 15px;
    line-height: 1.6;
    text-align: center;
    color: #fff;
    margin-bottom: 60px;
  }
  .duvidas-item-pergunta {
    display: flex;
    justify-content: space-between;
    padding: 10px;
    border: 1px solid #fff;
    border-radius: 20px;
    cursor: pointer;
  }
  .duvidas-item-pergunta h3{
    font-family: 'Open Sans', sans-serif;
    font-size: 14px;
    text-align: left;
    margin: 0;
    display: flex;
    align-content: center;
    align-self: center;
    font-weight: 600;
    color: #fff;
  }
  .duvidas-item{
    margin: 10px 0;
  }
  .duvidas-item-pergunta i{
    color: #fff;
    font-size: 20px;
    width: 20px;
    height: 20px;
    transition: 500ms;
    transform: rotate(-90deg);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .duvidas-item-pergunta i.duvidasItemActive{
    transform: rotate(0deg);
  }
  .duvidas-item-resposta {
    margin: 10px 20px;
  }
  .duvidas-item-resposta p {
    font-family: 'Open Sans', sans-serif;
    color: #fff;
    text-align: justify;
    font-size: 14px;
    line-height: 1.4;
  }

  /* COMPRA SEGURA */
  #seguranca {
    margin-top: 45px;
    padding: 30px 0px 50px;
    background-color: #f9f9f9;
  }
  .seguranca-t1{
    font-size: 36px;
    font-weight: 500;
    line-height: 1;
    text-align: center;
    color: #404040;
  }
  .seguranca-t2{
    margin-top: 10px;
    font-size: 15px;
    line-height: 1.6;
    text-align: center;
    color: #888;
    margin-bottom: 30px;
  }
  .seguranca-img{
    flex: 1 1 auto;
  }
  .seguranca-t3{
    margin-top: 10px;
    font-size: 18px;
    font-weight: 900;
    line-height: 1.3;
    color: #f13787;
    margin-bottom: 8px;
  }
  .seguranca-text{
    font-size: 14px;
    line-height: 1.4;
    color: #666666;
  }
  .columns:not(:last-child) .seguranca-text{
    margin-bottom: 10px;
  }

  /* VITRINE */
  #vitrineNews{
    margin-top: 45px;
  }
  /* ===================================================== */
</style>
