<template lang="html">
  <section class="vitrineDefault">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <slot></slot>
        </div>
        <div class="col-12">
          <div class="vitrineDefault-container" ref="containerVitrine">
            <div class="row align-middle">
              <div class="col-sm-12 col-md-4" v-for="(prod, i) in itensVitrine" :key="prod.id">
                <div class="vitrineDefault-container-item" :class="{itemDestaque: vitrineConfig[i] && vitrineConfig[i].destaque}">
                  <div class="vitrineDefault-container-item-top">

                    <!-- BLOCO TITLE PRODUTO-->
                    <div class="vitrineDefault-container-item-top-boxDesc" v-if="prod.precos.de > prod.precos.por">
                      <div class="vitrineDefault-container-item-top-boxDesc-desconto">
                        {{ Math.round(100 - (prod.precos.por * 100 / prod.precos.de)) }}% <br>OFF
                      </div>
                      <div class="vitrineDefault-container-item-top-boxDesc-descricao" v-html="prod.descricoes.longa"></div>
                    </div><!--top-boxDesc-->


                    <div class="" v-if="prod.descricoes && prod.descricoes.opcional1" v-html="prod.descricoes.opcional1"></div>

                    <!-- BLOCO IMAGEM PRODUTO -->
                    <div class="vitrineDefault-container-item-top-img">
                      <template v-if="prod.selos.length > 0">
                        <div class="vitrineSelo" :class="[selo.posicao.x, selo.posicao.y]" v-for="selo in prod.selos" :key="selo.id">
                          <img :src="selo[tipoImg.banner]" :alt="selo.nome" v-if="selo[tipoImg.banner] !== ''">
                          <span v-if="selo[tipoImg.banner] === ''" :style="{color: selo.cores.texto, backgroundColor: selo.cores.selo}">
                            {{ selo.label }}
                          </span>

                        </div>
                      </template>
                      <img :src="prod.midias.imagens.length > 0 ? prod.midias.imagens[0][tipoImg.produto].medium : require(`@/${$imgDefaultM}`)" :alt="prod.midias.imagens > 0 ? prod.midias.imagens[0].label : ''" @click.ctrl.exact="openNewtab(prod.url)" @click.middle.exact="openNewtab(prod.url)">
                      <div class="mascara-frete" style="position:relative;">
                        <img style="
                        position: absolute;
                        top: -150px;
                        left: 0;
                        max-width: 40% !important;"
                        src="@/assets/img/mascara-FRETE.png"/>
                      </div>
                    </div><!---container-item-top-img-->




                    <div class="vitrineDefault-container-item-top-nome">
                      <div class="vitrineDefault-container-item-top-nome-container">
                        <b>Contém: </b>
                        <h4>{{ prod.nome }}</h4>
                      </div>
                    </div>


                    <cronometro :cronData="vitrineConfig[i].cronometro"  v-if="vitrineConfig[i] && vitrineConfig[i].cronometro.ativo" />
                    <div class="boxAvliacaoStars" v-if="prod.avaliacao.quantidade > 0">
                      <div class="boxAvliacaoStars-yellow" :style="{width: `${prod.avaliacao.media * 20}%`}"></div>
                    </div>
                  </div><!--vitrineDefault-container-item-top-->

                  <div class="vitrineDefault-container-item-bottom">
                    <template v-if="prod.status == 'disponivel'">
                      <div class="vitrineDefault-container-item-bottom-precoDe" v-if="prod.precos.de > prod.precos.por">
                        De: {{ $formatPrice(prod.precos.de) }}
                      </div>
                      <div class="vitrineDefault-container-item-bottom-precoPor">
                        Por apenas: <b>{{ $formatPrice(prod.precos.vista) }}</b>
                      </div>
                      <div class="vitrineDefault-container-item-bottom-ou">
                        <img src="@/assets/img/img-ou.png" alt="">
                      </div>
                      <div class="vitrineDefault-container-item-bottom-condicao" v-html="$stringParcelamentoProds(prod.precos.parcelamento)"></div>
                      <button @click="addCart(prod.carrinho)" class="vitrineDefault-container-item-bottom-bt" :class="[vitrineConfig[i] ? vitrineConfig[i].tipo : '', vitrineConfig[i] ? {destaque: vitrineConfig[i].destaque} : '']">
                        <div>
                          COMPRE AGORA
                        </div>
                      </button>

                      <div class="vitrineDefault-container-item-bottom-frete">
                        <img src="@/assets/img/ico-frete-gratis.png" alt="">
                      </div>
                    </template>

                    <template v-if="prod.status == 'sobConsulta'">
                      <span class="vitrineAlerta">Sob consulta</span>
                      <router-link tag="button" :to="{...prod.rota}" class="vitrineDefault-container-item-bottom-bt">
                        <span @click.ctrl.exact="openNewtab(prod.url)" @click.middle.exact="openNewtab(prod.url)">
                          Solicitar orçamento
                        </span>
                      </router-link>
                    </template>

                    <template v-if="prod.status == 'indisponivel'">
                      <span class="vitrineAlerta">Produto indisponível</span>
                      <router-link tag="button" :to="{...prod.rota}" class="vitrineDefault-container-item-bottom-bt aviseMe">
                        <span @click.ctrl.exact="openNewtab(prod.url)" @click.middle.exact="openNewtab(prod.url)">
                          Avise-me quando chegar
                        </span>
                      </router-link>
                    </template>
                  </div><!--vitrineDefault-container-item-top-->
                </div><!--vitrineDefault-container-item-->
              </div><!--small-12 medium-4 columns-->
            </div><!--row-->

          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss" scoped>
  #app > div:nth-child(5) > main > div > section:nth-child(3) > div > div > div:nth-child(2) > div > div > div:nth-child(1) > div > div.vitrineDefault-container-item-top > div.vitrineDefault-container-item-top-img > div > img{
      display:none !important;
  }
  #app > div:nth-child(5) > main > div > section:nth-child(5) > div > div > div:nth-child(2) > div > div > div:nth-child(1) > div > div.vitrineDefault-container-item-top > div.vitrineDefault-container-item-top-img > div > img{
    display:none !important;
  }
  #app > div:nth-child(5) > main > div > section:nth-child(5) > div > div > div:nth-child(2) > div > div > div:nth-child(2) > div > div.vitrineDefault-container-item-top > div.vitrineDefault-container-item-top-img > div > img{
    display:none !important;
  }
  #app > div:nth-child(5) > main > div > section:nth-child(5) > div > div > div:nth-child(2) > div > div > div:nth-child(3) > div > div.vitrineDefault-container-item-top > div.vitrineDefault-container-item-top-img > div > img{
    display: none !important;
  }
</style>
<script>
import Comunicacao from '@/comunicacao.js'
import { mapGetters } from 'vuex'
export default {
  components: {
    cronometro: () => import('@/components/gerais/vitrine/cronometro.vue'),
  },
  props: {
    vitrineData: Array,
  },
  data() {
    return {
      itensVitrine: this.vitrineData,
      horas: '00',
      minutos: '00',
      segundos: '00',
    }
  },
  computed: {
    ...mapGetters(['tipoImg']),
    vitrineConfig() {
      let data = [], dataItem;
      this.vitrineData.forEach((item, i) => {
        dataItem = item.descricoes.opcional2.replace(/<\/?p>/g, '');
        data[i] = item.descricoes.opcional2.length > 0 ? JSON.parse(dataItem) : null;
      });
      return data;
    }
  },
  methods: {
    vitrineCronometro() {
      const actualDate = new Date();
      this.horas = 23 - actualDate.getHours();
      this.horas = this.horas.toString().length < 2 ? '0'+this.horas.toString() : this.horas.toString();
      this.minutos = 59 - actualDate.getMinutes();
      this.minutos = this.minutos.toString().length < 2 ? '0'+this.minutos.toString() : this.minutos.toString();
      this.segundos = 59 - actualDate.getSeconds();
      this.segundos = this.segundos.toString().length < 2 ? '0'+this.segundos.toString() : this.segundos.toString();
    },
    addCart(dadosCarrinho) {
      Comunicacao.$emit('toggleLoader', true);
      let {tipo, itens} = dadosCarrinho;
      let itemAdc       = false
      if (tipo && itens) {
        //ADICIONA O PRODUTO AO CARRINHO
        this.$carrinho.add(tipo,itens,(success, response) => {

          response.data.itens.forEach(prod => {
            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == dadosCarrinho.itens[0].idProduto;
          });
          //PRODUTO ADICIONADO COM SUCESSO
          if(success) return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data });
          //PROBLEMAS AO ADICIONAR PRODUTO
          alert('Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.');
        });
        return;
      }
    }
  },
  created() {
    setInterval(() => {
      this.vitrineCronometro();
    }, 1000);
  }
}
</script>

<style lang="css" scoped>
.vitrineDefault{
  margin-bottom: 50px;
}
.vitrine-t2{
  text-align: center;
  color: #888;
  font-size: 15px;
  margin-bottom: 20px;
  line-height: 1.3;
}
.vitrineDefault-container{
  display: flex;
}
.vitrineDefault-container > .row{
  width: 100%;
}
.vitrineDefault-container-item{
  display: flex;
  flex-direction: column;
  padding: 0 20px 20px;
  border: 1px solid transparent;
  box-shadow: 0px 10px 30px rgb(171 171 171 / 60%);
  border: 1px solid #ddd;
  background-color: #fff;
}
.vitrineDefault-container-item-top{
  flex: 0 1 auto;
}
.vitrineDefault-container-item-top > a{
  display: block;
}
.vitrineDefault-container-item-top-img{
  position: relative;
  text-align: center;
}
.vitrineDefault-container-item.itemDestaque .vitrineDefault-container-item-top-nome-container{
  position: relative;
  top: 10px;
}
.vitrineDefault-container-item-top-nome{
  padding-bottom: 12px;
  border-bottom: 1px solid #ddd;
}
.vitrineDefault-container-item-top-nome b{
  font-size: 12px;
  line-height: 1.6;
  color: #444;
  display: inline;
}
.vitrineDefault-container-item-top-nome h4{
  font-size: 12px;
  line-height: 1.6;
  color: #888;
  display: inline;
}
.vitrineDefault-container-item-top-cronometro{
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #FF03A8;
  color: #fff;
  margin: 0 -20px;
  padding: 5px 0;
}
.vitrineDefault-container-item-top-cronometro-tempo{
  margin-left: 15px;
}
.vitrineDefault-container-item-top-cronometro-tempo-text{
  font-size: 14px;
  color: #fff;
  font-weight: bold;
  line-height: 1;
}
.vitrineDefault-container-item-top-cronometro-tempo-num{
  display: flex;
  font-weight: bold;
  font-size: 34px;
  color: #fff;
  line-height: 1;
}
.vitrineDefault-container-item-bottom{
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  padding-top: 20px;
  text-align: center;
}
.vitrineDefault-container-item-bottom-precoDe{
  font-size: 20px;
  text-decoration: line-through;
  color: #888;
  line-height: 1;
  margin-bottom: 5px;
}
.vitrineDefault-container-item-bottom-precoPor{
  font-size: 20px;
  color: #888;
  line-height: 1;
}
.vitrineDefault-container-item-bottom-precoPor b{
  color: #000;
}
.vitrineDefault-container-item-bottom-ou{
  margin-top: 10px;
  margin-bottom: 5px;
}
.vitrineDefault-container-item-bottom-precoMsg{
  font-size: 12px;
  line-height: 1.166;
  display: block;
  color: #43A047;
  margin-bottom: 15px;
}
.vitrineDefault-container-item-bottom-condicao{
  font-size: 20px;
  display: flex;
  flex-direction: column;
}
.vitrineDefault-container-item-bottom-divisor{
  max-width: 90px;
  margin-bottom: 10px;
  margin-top: 10px;
  border-bottom: 1px solid #707070;
  width: 100%;
  display: block;
}
.vitrineDefault-container-item-bottom-bt{
  background: #04b900;
  color: #fff;
  font-size: 15px;
  font-weight: bold;
  padding: 20px 50px 20px 50px;
  border-radius: 5px;
  letter-spacing: 0px;
  transition: all 0.3s ease;
  margin-top: 10px;
  font-family: 'Open sans', sans-serif;
  transition: 400ms ease;
}
.vitrineDefault-container-item-bottom-bt div{
  min-height: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.vitrineDefault-container-item-bottom-bt.mulher.destaque{
  background-color: #ff03a8;
}
.vitrineDefault-container-item-bottom-bt:hover{
  opacity: .8;
}

.vitrineDefault-container-item-bottom-frete{
  margin: 20px 0 14px;
}

.vitrineAlerta{
  display: flex;
  text-align: center;
  font-size: 14px;
  color: #D22E2E;
  height: 100%;
  align-items: center;
  justify-content: center;
  margin-bottom: 10px;
}

.vitrineDefault-container-item-top-boxDesc{
  display: flex;
  margin: 0 -20px;
}
.vitrineDefault-container-item-top-boxDesc-desconto{
  padding: 15px 15px 15px 15px;
  font-weight: bold;
  font-size: 17px;
  line-height: 17px;
  color: #fff;
  background-color: #42C7A1;
}
.vitrineDefault-container-item-top-boxDesc-descricao{
  display: flex;
  flex: 1 1 auto;
}

@media (min-width: 768px) {
  .vitrineDefault-container {
    margin: 0 -0.9375rem;
    justify-content: center;
  }
}

/* ================================== MOBILE ================================== */
@media (max-width: 767px) {
  .vitrineDefault-container > .row{
    width: unset;
  }
  .col-md-4:not(:last-child) > .vitrineDefault-container-item{
    margin-bottom: 20px;
  }
}
</style>


<style>
.vitrineDefault-container-item-bottom-condicao b{
  font-size: 45px;
  color: #000;
}
</style>
