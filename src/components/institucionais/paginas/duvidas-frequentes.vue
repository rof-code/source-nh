<template lang="html">
  <section>
    <div class="duvidasContainer-topo">
      <h1 class="vitabe-t1"> Perguntas Frequentes </h1>
      <p class="vitabe-t2"> Veja as principais dúvidas dos nossos clientes. </p>
      <p class="vitabe-t2"> Caso ainda tenha alguma pergunta que não apontamos aqui, fale com um de nossos canais de atendimento. </p>
    </div>
    <div class="duvidasContainer">
      <div class="duvidasContainer-item" v-for=" (item, i) in itens " :key=" i ">
        <p class="institucional-t1" @click=" $slideToggle($refs[`faq${i}`][0]); $event.target.classList.toggle('ativo') ">
          {{ item.pergunta }}
          <i class="fa fa-caret-right"></i>
        </p>
        <div :ref=" `faq${i}` " class="duvidasContainer-item-text">
          <p v-html="item.resposta"></p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      itens: [
        {
          pergunta: "Como devo usar New Hair?",
          resposta:
            "A dose diária a ser tomada é de uma cápsula ao dia. Como durante o período da manhã a absorção dos nutrientes é facilitada e os resultados otimizados, sugerimos que tome New Hair após sua primeira refeição. ",
        },
        {
          pergunta: "New Hair engorda?",
          resposta:
            "Não, as cápsulas têm componentes 100% naturais e de rápida absorção, sem nenhum tipo de lipídio ou agente que cause efeitos colaterais no corpo. ",
        },
        {
          pergunta: "New Hair possui contraindicação?",
          resposta:
            "Não tem contraindicação. Porém, caso tenha algum tipo de alergia, indicamos que verifique os componentes da fórmula antes de fazer o uso.",
        },
        {
          pergunta: "Estimula o crescimento em outras áreas do corpo?",
          resposta:
            "A formulação do New Hair, assim como de outros complexos vitamínicos, não atua em níveis hormonais, apenas em regiões onde já existem folículos capilares. Então pode ficar tranquila! O New Hair não estimula o crescimento de pelos em outras partes do corpo e nem interfere em procedimentos estéticos como depilação a laser.",
        },
        {
          pergunta: "Grávidas ou lactantes podem utilizar?",
          resposta:
            "O New Hair pode ser tomado mesmo amamentando, pois é um complexo vitamínico e mineral 100% natural e não possui contraindicações. Nosso produto possui componentes que irão auxiliar no fortalecimento dos fios e combater a queda causada nesse período de amamentação. No caso de gravidez, leve a fórmula ao médico para melhor orientação. ",
        },
        {
          pergunta: "New Hair pode ser consumido em qualquer idade?",
          resposta:
            "Sugerimos que crianças menores de 12 anos façam a utilização do produto apenas sob orientação profissional. ",
        },
        {
          pergunta: "New Hair interfere no anticoncepcional?",
          resposta:
            "Como nossos produtos são compostos apenas de nutrientes naturais, não há contraindicações e nem interações medicamentosas reconhecidas. ",
        },
        {
          pergunta: "Em quanto tempo sentirei os efeitos das vitaminas?",
          resposta:
            "Os resultados de New Hair variam de pessoa para pessoa. Porém, desde a primeira semana de tratamento você perceberá uma redução significativa da queda de cabelo, além de fios mais fortes, saudáveis e brilhantes. Para melhores resultados quanto ao crescimento dos fios, indicamos um tratamento mínimo de 3 meses com New Hair, além do uso contínuo para que seus cabelos se mantenham lindos e saudáveis. ",
        },
        {
          pergunta: "Pode ser usado com química?",
          resposta:
            "Claro! Uma vez que New Hair auxilia seu cabelo a crescer mais forte e saudável, ele pode ser um super aliado contra os efeitos da química. Tomando New Hair, você terá fios mais fortes e resistentes para aguentar a química sem sofrer grandes danos. ",
        },
        {
          pergunta: "New Hair é liberado pela Anvisa?",
          resposta:
            "O New Hair é dispensado de registro da Anvisa por estar de acordo com a RDC 240/2018 na categoria 4300041-Suplemento Vitamínico ou Mineral. ",
        },
        {
          pergunta: "Qual o prazo de entrega?",
          resposta:
            "O New Hair é despachado em média de 24h úteis após aprovação do pagamento, mas dependemos da agilidade dos Correios para que as entregas sejam feitas até o seu endereço. <br> Abaixo os prazos médios: <br> <ul><li>Região Sudeste - de 3 a 5 dias </li> <li>Região Sul - de 4 a 6 dias </li> <li>Região Centro-Oeste - de 4 a 6 dias </li> <li>Região Nordeste - de 5 a 10 dias </li> <li>Região Norte - de 7 a 17 dias </li></ul>",
        },
        {
          pergunta: "Quais as formas de pagamento?",
          resposta:
            "Disponibilizamos as seguintes maneiras para você efetuar o pagamento do seu pedido: <br > <br >Cartão de Crédito: - Visa, Mastercard, Diners, Elo, Amex e Hipercard. <br >  <br > Pagamento à vista Boleto Bancário: O prazo de vencimento do boleto bancário é de 2 dias úteis contados a partir da data de emissão. Importante! Os itens comprados só são reservados até o vencimento do boleto. ",
        },
      ],
    };
  },
};
</script>

<style lang="css" scoped>
section {
  margin-bottom: 90px;
}
.duvidasT1 {
  display: block;
  color: #444;
  font-size: 14px;
}
.duvidasContainer-topo {
  margin: 40px 0 0;
}
.institucional-t1 {
  border-bottom: 1px solid #dbdbdb;
}
.duvidasContainer {
  overflow: hidden;
  border-radius: 4px;
}
.duvidasContainer-item {
  padding: 10px 0 0;
  border-bottom: none;
}
.duvidasContainer-item-text {
  overflow: hidden;
  display: none;
}
.duvidasContainer-item-text p {
  font-size: 14px;
  display: block;
  color: #828282;
  text-align: justify;
  padding: 10px;
}
.institucional-t1 i {
  transition: 200ms;
}
.institucional-t1.ativo i {
  transform: rotate(90deg);
}
@media (max-width: 767px) {
  .institucional-t1 {
    font-size: 14px;
  }
  .duvidasContainer-topo {
    margin: 0;
  }
}
</style>