<template>
    <header class="mobf justify-content-around" id="mobMenu">
        <li class="">
            <i class="fas fa-bars"></i>
        </li>

        <a href="/">
            <img class="logoMob" src="@/assets/img/logo_newhair.png" alt="">
        </a>

        <a :href="`${$siteUrl}/checkout/carrinho/`" @click.prevent="openCarrinho()">
            <svg xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg" data-v-2086c66c="" viewBox="0 0 34.5 30.3" class="icon-inline icon-2x" width="24"  height="22" ><path data-v-2086c66c="" d="M31 17.6l3-13-.1-.4-.4-.2H6.8L6 .4C5.9.2 5.7 0 5.5 0h-5C.2 0 0 .2 0 .5s.2.5.5.5h4.6L10 23.6l.2.3c-.7.6-1.2 1.6-1.2 2.6 0 1.9 1.6 3.5 3.5 3.5s3.5-1.6 3.5-3.5c0-1-.4-1.9-1.1-2.5H25c-.7.6-1.1 1.5-1.1 2.5 0 1.9 1.6 3.5 3.5 3.5s3.5-1.6 3.5-3.5-1.5-3.5-3.4-3.5H10.9l-1.1-5h20.7c.2 0 .4-.2.5-.4zm-1 8.9c0 1.4-1.1 2.5-2.5 2.5S25 27.9 25 26.5s1.1-2.5 2.5-2.5 2.5 1.1 2.5 2.5zm-15 0c0 1.4-1.1 2.5-2.5 2.5S10 27.9 10 26.5s1.1-2.5 2.5-2.5 2.5 1.1 2.5 2.5zM9.6 17L7 5h25.9l-2.8 12H9.6z" fill="#FFFFFF"></path></svg>
            <div class="headerContainerTop-carrinho-num">
            {{ dadosCarrinho.quantidadeItens }}
            </div>
        </a>

            <div class="overlayMenu"></div>
            <ul class="itensMenu">
                <div class="menuicon">
                    <div class="col-12 d-flex">
                        <div class="col-6">
                            <i class="fas fa-times"></i>
                        </div>
                        <div class="col-6">
                            <span>MENU</span>
                        </div>
                    </div>
                </div>
                <a href="/home">
                     <li><a href="/">HOME</a></li>
                </a>
                <a href="/pagina/atendimento">
                   <li><a href="/pagina/atendimento">ATENDIMENTO</a></li> 
                </a>
                <a href="/pagina/duvidas-frequentes">
                    <li><a href="/pagina/duvidas-frequentes">PERGUNTAS FREQUENTES</a></li>
                </a>
                <a href="/produtos">
                    <li><a href="/produtos">PRODUTOS</a></li>
                </a>
                <a href="/pagina/politica-de-privacidade">
                    <li><a href="/pagina/politica-de-privacidade">Políticas de Privacidade</a></li>
                </a>
                <a href="/pagina/termos">
                    <li><a href="/pagina/termos">Termos e Condições</a></li>
                </a>
                <a href="/pagina/revendedores-oficiais">
                    <li><a href="/pagina/revendedores-oficiais">Revendedores Oficiais</a></li>
                </a>
                <a href="/pagina/referencias-cientificas">
                    <li><a href="/pagina/referencias-cientificas">Referências Científicas</a></li>
                </a>
                <a href="https://www.newhaircaps.com.br/checkout/acesso">
                    <li><a href="https://www.newhaircaps.com.br/checkout/acesso">Meus Pedidos</a></li>
                </a>
               <a href="https://www.newhaircaps.com.br/checkout/acesso">
                   <li><a href="https://www.newhaircaps.com.br/checkout/acesso">Minha conta</a></li>
               </a>
                
            </ul>
    </header>
</template>
<script>
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
  },
  mounted() {
    var icon = document.querySelectorAll('.fas');
    var overlay = document.querySelector('.overlayMenu');
    var menu = document.querySelector('.itensMenu');
    icon.forEach(element => {
        element.addEventListener('click', () => {
        overlay.classList.toggle('activeOverlay');
        menu.classList.toggle('activeMenu');
        });
    });
    overlay.addEventListener('click', () => {
        overlay.classList.toggle('activeOverlay');
        menu.classList.toggle('activeMenu');
    });
    // var li = document.querySelectorAll('itensMenu li');
    // var ahrefs = document.querySelectorAll('.itensMenu li a');
    // console.log(ahrefs);
    // li.forEach(link => {
    //     link.addEventListener('click', () => {
    //         console.log('clickado');
    //     })
    // })
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

<style lang="scss" scoped>
    .itensMenu{
        transition: 0.5s ease;
        position:fixed;
        width:0;
        height:0;
        left:-200%;
        background-color:#fff;
        li{
            list-style-type: none;
            padding: 13px 0px 13px 30px;
            border-top: 1px solid #eee;

        }
        a{
            text-decoration: none;
            font-size:14px;
            text-transform: uppercase;
        }
    }
    .itensMenu{
        left:-200%;
        top:0;
    }
    .itensMenu.activeMenu{
        width:70vw;
        height:100vh;
        left:0;
        top:0;
        z-index:15;
        
    }
    .overlayMenu{
        transition:0.5s ease;
        width:100vw;
        height:100%;
        position:fixed;
        top:0;
        left:-200%;
        background-color:rgba(0,0,0,0.5);
    }
    .overlayMenu.activeOverlay{
        left:0;
        top:0;
        z-index:1;
    }
    .mobf{
        display: none;
    }
    .logoMob{
        position:relative;
        right:-5px;
    }
    .headerContainerTop-carrinho-num {
        position: absolute;
        top: 4%;
        right:23px;
        font-size: 10px;
        color: #fff;
        background-color: red;
        border-radius: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        padding:1px 5px;
    }
    header.mobf{
        padding:10px 0px;
        background-color:#ff2c7b;
        align-items:center;
        .menuicon{
            .col-12.d-flex{
                padding:20px;
            }
            span{
                color:#000;
                font-size:25px;
                font-weight:bold;
            }
            i{
                color:#000;
                font-size:35px;
            }
        }
        i{
            color:#fff;
            font-size:25px;
        }
        li{
            list-style-type: none;
        }
        .svgCart{
            position:relative;
            left:-5px;
        }
    }
    @media screen and (max-width: 800px){
    .mobf{
        display: flex;
    }
    }
</style>