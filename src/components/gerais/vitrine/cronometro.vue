<template lang="html">
  <div class="vitrineDefault-container-item-top-cronometro">
    <div class="vitrineDefault-container-item-top-cronometro-img">
      <img src="@/assets/img/geral/relogio.png" alt="">
    </div>
    <div class="vitrineDefault-container-item-top-cronometro-tempo">
      <p class="vitrineDefault-container-item-top-cronometro-tempo-text">OFERTA EXPIRA EM:</p>
      <div class="vitrineDefault-container-item-top-cronometro-tempo-num">
        <div class="">
          {{ horas }}
        </div>
        :
        <div class="">
          {{ minutos }}
        </div>
        :
        <div class="">
          {{ segundos }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    cronData: Object,
  },
  data() {
    return {
      horas: '00',
      minutos: '00',
      segundos: '00',
    }
  },
  computed: {
    finalDate() {
      return new Date(this.cronData.dataFinal)
    }
  },
  methods: {
    vitrineCronometroInfinito() {
      const actualDate = new Date();

      this.horas = 23 - actualDate.getHours();
      this.horas = this.horas.toString().length < 2 ? '0'+this.horas.toString() : this.horas.toString();

      this.minutos = 59 - actualDate.getMinutes();
      this.minutos = this.minutos.toString().length < 2 ? '0'+this.minutos.toString() : this.minutos.toString();

      this.segundos = 59 - actualDate.getSeconds();
      this.segundos = this.segundos.toString().length < 2 ? '0'+this.segundos.toString() : this.segundos.toString();
    },
    vitrineCronometro() {
      const actualDate = new Date().getTime();

      this.segundos = (this.finalDate.getTime() - actualDate) / 1000;

      this.horas = parseInt(this.segundos / 3600);
      this.segundos = this.segundos % 3600;

      this.minutos = parseInt(this.segundos / 60);
      this.segundos = parseInt(this.segundos % 60);

      this.horas =  Math.abs(this.horas);
      this.segundos =  Math.abs(this.segundos);
      this.minutos =  Math.abs(this.minutos);

      this.horas < 10 ? this.horas =  "0" + this.horas  : this.horas;
      this.segundos < 10 ? this.segundos =  "0" + this.segundos  : this.segundos;
      this.minutos < 10 ? this.minutos =  "0" + this.minutos  : this.minutos;

    },
    startChronometer() {
      if (this.cronData.infinito) {
        setInterval(() => {
          this.vitrineCronometroInfinito();
        }, 1000);
        return;
      }
      setInterval(() => {
        this.vitrineCronometro();
      }, 1000);
    }
  },
  created() {
    this.startChronometer();
  }
}
</script>

<style lang="css" scoped>
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
</style>
