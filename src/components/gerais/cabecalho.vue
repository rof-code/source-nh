<template lang="html">
 <skeletonMainMenu class="menuSkeleton" v-if="!menuLoaded && screenWidth > 1023" />
  <header v-else>

    <vendaInterna
    :dados="dadosUser"
    :carrinho="dadosCarrinho"
    v-if="dadosUser && dadosCarrinho && Object.keys(dadosUser.vendaInterna).length > 0 && dadosUser.vendaInterna.id"/>
    <div class="container">
      <div class="row align-center">
        <div class="col-12 headerContainerTop">
          <button type="button" name="button" class="material-icons headerContainerTop-menu" @click="openMenu()">
            menu
          </button>

          <div class="headerContainerTop-buscaContainer">
            <div class="headerContainerTop-buscaContainer-top">
              <transition name="fadeNoDelay">
                <mainMenu v-if="menuLoaded && dadosUser" :dadosUser="dadosUser" />
              </transition>
            </div>
          </div>

          <div class="headerContainerTop-logo">
            <router-link :to="{ name: 'home', params: {} }">
              <img :src="require('@/assets/img/geral/logo-feminino.png')" alt="">
            </router-link>
          </div>


          <div class="headerContainerTop-buscaContainer" >
            <div class="headerContainerTop-buscaContainer-top">
              <template v-if="screenWidth > 1023">
                <div class="headerContainerTop-user-text" v-if="!dadosUser.logado">
                  <p class="headerContainerTop-user-text-logar">
                    <a :href="`${$siteUrl}/checkout/acesso`">Minha Conta</a>
                  </p>
                </div>
                <div class="headerContainerTop-user-text logado" v-if="dadosUser.logado">
                  <i class="fa fa-user"></i> <a :href="`${$siteUrl}/minha-conta/`">{{dadosUser.email}} </a>
                  | <a :href="`${$siteUrl}/minha-conta/`">Sair</a>
                </div>
                <router-link to="/pagina/atendimento"><p>atendimento</p></router-link>
              </template>
              <div class="headerContainerTop-carrinho">
                <a :href="`${$siteUrl}/checkout/carrinho/`" @click.prevent="openCarrinho()">
                  <svg class="icon-inline icon-2x" viewBox="0 0 34.5 30.3"><path d="M31 17.6l3-13-.1-.4-.4-.2H6.8L6 .4C5.9.2 5.7 0 5.5 0h-5C.2 0 0 .2 0 .5s.2.5.5.5h4.6L10 23.6l.2.3c-.7.6-1.2 1.6-1.2 2.6 0 1.9 1.6 3.5 3.5 3.5s3.5-1.6 3.5-3.5c0-1-.4-1.9-1.1-2.5H25c-.7.6-1.1 1.5-1.1 2.5 0 1.9 1.6 3.5 3.5 3.5s3.5-1.6 3.5-3.5-1.5-3.5-3.4-3.5H10.9l-1.1-5h20.7c.2 0 .4-.2.5-.4zm-1 8.9c0 1.4-1.1 2.5-2.5 2.5S25 27.9 25 26.5s1.1-2.5 2.5-2.5 2.5 1.1 2.5 2.5zm-15 0c0 1.4-1.1 2.5-2.5 2.5S10 27.9 10 26.5s1.1-2.5 2.5-2.5 2.5 1.1 2.5 2.5zM9.6 17L7 5h25.9l-2.8 12H9.6z"></path></svg>
                  <div class="headerContainerTop-carrinho-num">
                    {{ dadosCarrinho.quantidadeItens }}
                  </div>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>


  </header>
</template>

<script>
import comunicacao from "@/comunicacao.js";
import { mapState, mapMutations } from 'vuex';

export default {
  components: {
    mainMenu: () => import("@/components/gerais/cabecalho/menu.vue"),
    skeletonMainMenu: () =>
      import("@/components/skeletons/geral/cabecalho.vue"),
    vendaInterna: () =>
      import("@/components/gerais/cabecalho/topo-venda-interna.vue"),
  },
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
  },
  created() {
    comunicacao.$on(
      "updateNumCarrinho",
      (qtd) => (this.dadosCarrinho.quantidadeItens = qtd)
    );
  },
};
</script>

<style lang="css" scoped>
header {
  background: #ff478b;
  padding: 10px;
}
.headerContainerTop {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* LOGO */
.headerContainerTop-logo {
  margin-right: 70px;
}

/* BUSCA */

.headerContainerTop-buscaContainer-top {
  color: #fff;
  font-size: 10px;
  display: flex;
  line-height: 1;
  text-transform: uppercase;
  font-weight: 700;
}
.headerContainerTop-buscaContainer-top p {
  margin-bottom: 0;
}
.headerContainerTop-buscaContainer-top div {
  display: flex;
  align-items: center;
}
.headerContainerTop-buscaContainer-top a {
  margin-right: 40px;
  display: flex;
  align-items: center;
}
.headerContainerTop-buscaContainer-top .headerContainerTop-carrinho a {
  margin-right: 0px;
}
.headerContainerTop-buscaContainer-top a span {
  margin-right: 5px;
}

/* CONTAINER DO USUÁRIO */
.headerContainerTop-user {
  display: flex;
  align-items: center;
  margin-right: 25px;
  align-self: flex-end;
}
.headerContainerTop-user-icone {
  margin-right: 10px;
}
.headerContainerTop-user-text {
  color: #fff;
  line-height: 1.1538;
  white-space: nowrap;
}
.headerContainerTop-user-text.logado {
  font-size: 11px;
  text-transform: none;
  margin-right: 40px;
}
.headerContainerTop-user-text.logado a {
  margin: 0 10px;
}
.headerContainerTop-user-text .fa.fa-user {
  font-size: 13px;
}
/* CARRINHO */
.headerContainerTop-carrinho {
  position: relative;
  flex: 0 1 auto;
}

.headerContainerTop-carrinho svg {
  font-size: 20px !important;
  fill: #fff;
  height: 18px;
  width: 21px;
  max-width: 100%;
}
.headerContainerTop-carrinho-num {
  --tamanho: 16px;
  position: absolute;
  top: -5px;
  right: -10px;
  height: var(--tamanho);
  width: var(--tamanho);
  font-size: 10px;
  color: #fff;
  background-color: red;
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* WHATSAPP */
.headerContainerTop-whats {
  align-self: flex-end;
  margin-right: 25px;
}
.headerContainerTop-whats-container {
  display: flex;
  color: #fff;
}
.headerContainerTop-whats-container-text {
  font-size: 13px;
  margin-left: 10px;
  white-space: nowrap;
}
.headerContainerTop-whats-container-text b {
  display: block;
}

/* BOTÃO MENU */
.headerContainerTop-menu {
  display: none;
}
.menuSkeleton {
  margin-top: 15px;
}

/************************ TABLET ************************/
@media (min-width: 768px) and (max-width: 1023px) {
  header {
    padding-bottom: 10px;
  }
}
@media (max-width: 1023px) {
  .headerContainerTop-carrinho svg {
    height: 20px;
    width: 22px;
  }
  /* WHATSAPP */
  .headerContainerTop-whats {
    display: none;
  }

  /* MENU */
  .headerContainerTop-menu {
    color: #fff;
    font-size: 33px;
    margin-right: 10px;
    display: block;
  }
  .headerContainerTop-logo {
    margin-right: 30px;
    text-align: center;
  }
  .headerContainerTop-user-text {
    display: none;
  }
  .headerContainerTop-user {
    margin-right: 20px;
  }
  .headerContainerTop-user-icone {
    margin-right: 0;
  }
}

/************************ MOBILE ************************/
@media (max-width: 767px) {
  /* LOGO */
  .headerContainerTop-logo {
    flex: 1 1 auto;
    margin: 0;
    display: block;
    margin: 0 auto;
  }
  .headerContainerTop-logo svg {
    max-width: 150px;
  }

  /* BUSCA */

  .headerContainerTop-buscaContainer {
    order: 2;
  }
  /* USUÁRIO */
  .headerContainerTop-user {
    margin-right: 20px;
    max-width: 20px;
  }
  .headerContainerTop-user-icone {
    max-width: 20px;
    display: flex;
  }
  .headerContainerTop-user-text {
    display: none;
  }

  /* CARRINHO */
  .headerContainerTop-carrinho {
    display: flex;
    margin-right: 10px;
    align-self: center;
  }
  .headerContainerTop-carrinho svg {
    max-width: 26px;
  }

  /* BUSCA */
  .headerContainerTop-buscaContainer {
    max-width: 100%;
  }
}
</style>
