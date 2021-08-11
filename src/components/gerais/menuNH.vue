<template>
    <header class="desk" id="deskMenu">
        <section class="header">
            <div class="headerDesk">
                <nav class="navbar navbar-expand-lg">
                    <div class="container">
                        <ul class="navbar-nav mr-auto">
                            <li class="nav-item">
                                <a href="/produtos" class="nav-link pedidoTop">GUMMIES</a>
                            </li>
                            <li class="nav-item">
                                <a href="/produtos" class="nav-link" id="scrollCaps">CÁPSULAS</a>
                            </li>
                            <li class="nav-item">
                                <a href="https://www.newhaircaps.com.br/newhair-masculino" class="nav-link">MASCULINO</a>
                            </li>
                        </ul>
                        <a href="/" class="navbar-brand mx-auto">
                            <img src="@/assets/img/logo_newhair.png" alt="">
                        </a>
                        <ul class="navbar-nav ml-auto ulDireita">
                            <li class="nav-item">
                                <a href="https://www.newhaircaps.com.br/checkout/acesso" class="nav-link">MINHA CONTA</a>
                            </li>
                            <li class="nav-item">
                                <a href="/pagina/atendimento" class="nav-link">ATENDIMENTO</a>
                            </li>
                            <li class="nav-item">
                                <a :href="`${$siteUrl}/checkout/carrinho/`" @click.prevent="openCarrinho()">
                                   <svg xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg" data-v-2086c66c="" viewBox="0 0 34.5 30.3" class="icon-inline icon-2x" width="21"  height="18" ><path data-v-2086c66c="" d="M31 17.6l3-13-.1-.4-.4-.2H6.8L6 .4C5.9.2 5.7 0 5.5 0h-5C.2 0 0 .2 0 .5s.2.5.5.5h4.6L10 23.6l.2.3c-.7.6-1.2 1.6-1.2 2.6 0 1.9 1.6 3.5 3.5 3.5s3.5-1.6 3.5-3.5c0-1-.4-1.9-1.1-2.5H25c-.7.6-1.1 1.5-1.1 2.5 0 1.9 1.6 3.5 3.5 3.5s3.5-1.6 3.5-3.5-1.5-3.5-3.4-3.5H10.9l-1.1-5h20.7c.2 0 .4-.2.5-.4zm-1 8.9c0 1.4-1.1 2.5-2.5 2.5S25 27.9 25 26.5s1.1-2.5 2.5-2.5 2.5 1.1 2.5 2.5zm-15 0c0 1.4-1.1 2.5-2.5 2.5S10 27.9 10 26.5s1.1-2.5 2.5-2.5 2.5 1.1 2.5 2.5zM9.6 17L7 5h25.9l-2.8 12H9.6z" fill="#FFFFFF"></path></svg>
                                    <div class="headerContainerTop-carrinho-num">
                                    {{ dadosCarrinho.quantidadeItens }}
                                    </div>
                                </a>
                            </li>
                        </ul>
                    </div>
                </nav>
            </div><!--headerDesk-->
        </section>
    </header>
</template>


<script>
// import $ from 'jquery';
import comunicacao from "@/comunicacao.js";
import { mapState, mapMutations } from 'vuex';
export default {
  data() {
    return {
      config: false,
      dadosCarrinho: false,
    };
  },
  computed: {
    ...mapState(['screenWidth', 'menuLoaded', 'dadosUser'])
  },
  methods: {
    ...mapMutations(['changeStatusMenu']),
    openMenu() {
      comunicacao.$emit("openMenu");
    },
    openCarrinho() {
      comunicacao.$emit("toggleCarrinho", { show: true });
    },
    // scrollCaps(){
    //   (function(){
    //     var btnCaps = document.getElementById('btn2');
    //     btnCaps.click();
    //   });
    //   document
    //   .getElementById('scrollCaps')
    //   .addEventListener('click', () => {
    //           let hash = this.getAttribute('href');
    //           let target = document.querySelector(hash);
    //           let headerOffset = 100;
    //           let elementPosition = target.offsetTop;
    //           let offsetPosition = elementPosition - headerOffset;
    //           window.scrollTo({
    //               top: offsetPosition,
    //               behavior: "smooth"
    //           });
    // });
    // }
  },
  mounted() {
    comunicacao.$on("updateSubTotal", (response) => {
      this.subTotalCarrinho = response.valor;
    });

    this.$requestSend(
      "get",
      "/v2/front/checkout/cart",
      {},
      (success, response) => {
        this.dadosCarrinho = response.data;
        if (
          response.data &&
          response.data.subtotal &&
          response.data.subtotal.valor
        ) {
          this.dadosSubTotal = response.data.subtotal.valor;
        }
        comunicacao.$emit("carrinhoCarregado", response.data);
      }
    );

    comunicacao.$on("configCarregada", (response) => {
      this.config = response.configuracoes;
    });

    this.$requestSend(
      "get",
      "/v2/front/checkout/cart",
      {},
      (success, response) => {
        this.dadosCarrinho = response.data;
        comunicacao.$emit("carrinhoCarregado", response.data);
      }
    );
    var capsRow = document.getElementById('capsRow');
    var linkCaps = document.getElementById('scrollCaps');
    linkCaps.addEventListener('click', () => {
      capsRow.scrollIntoView({behavior: "smooth"});
    })
    },
  created() {
    comunicacao.$on(
      "updateNumCarrinho",
      (qtd) => (this.dadosCarrinho.quantidadeItens = qtd)
    );
  },
};
</script>


<style lang="scss" scoped>
header.desk{
  display:block !important;
}
    .headerDesk{
        background-color:#ff2c7b;
        position:relative;
        li.nav-item{
            margin:0px 20px;
        }
        a.nav-link{
            color:#fff;
            font-size:10px;
            font-family: 'Roboto',sans-serif;
            font-weight: bold;
        }
        .container, ul.navbar-nav{
            align-items: center;
        }
        ul.ulDireita{
            position:relative;
        }
        .headerContainerTop-carrinho-num {
        position: absolute;
        top: -2px;
        right:10px;
        font-size: 10px;
        color: #ff2c7b;
        background-color: #fffc00;
        border-radius: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding:1px 6px;
        }
    }
@media screen and (max-width:768px){
  header.desk{
    display:none !important;
  }
}
</style>