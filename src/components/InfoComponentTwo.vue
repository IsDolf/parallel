<template>
  <div
    class="rounded-4 rounded-start py-2 mb-5 mt-4 special-box-shadow info-tab"
    @click="this.$emit('onama-two-toggle')"
  >
    <p class="mx-3 my-1 info-title">Popis programa</p>
    <p class="mx-3 my-1 info-text">
      Matematika, Fizika, Kemija, Biologija, Hrvatski jezik, Engleski jezik,
      Informatika, Povijest, Geografija, Tehnička kultura, Statistika,
      Programiranje, Osnove elektrotehnike, Računalstvo, Mjerenja u
      elektrotehnici, Uvod u elektroniku, Elektronika, Elektrotehnika, Opća i
      anorganska kemija, Organska kemija, Analitička kemija, Biokemija,
      Fizikalna kemija, Mikrobiologija, Stabilnost broda, Poznavanje broda,
      Rukovanje teretom, Astronomska navigacija, Terestrička navigacija,
      Elektronička navigacija, Brodski strojevi i uređaji, Tehnička mehanika,
      Tehnički materijali, Termodinamika Hidraulika i pneumatika Robotika,
      Industrijska automatizacija, Regulacija i upravljanje
    </p>
  </div>
</template>

<script>
export default {
  emits: ['onama-two-toggle'],
  data() {
    return {
    };
  },
};
</script>

<style scoped>
.special-box-shadow {
  box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px,
    rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;

  border: 1px solid rgba(156, 252, 248, 1) 11.2%, rgba(110, 123, 251, 1) 91.1%;
}
.info-tab {
  display: inline-block;
  width: 95vw;
  background: rgb(5, 218, 255);
  color: rgb(0, 7, 101);
}
.info-tab:hover {
  color: rgb(0, 10, 148);
  cursor: pointer;
  box-shadow: rgba(0, 0, 0, 0.4) 0px 1px 2px,
    rgba(0, 0, 0, 0.3) 0px 3.5px 6.5px -1.5px,
    rgba(0, 0, 0, 0.2) 0px -1.5px 0px inset;
}

.info-title {
  width: 90vw;
  font-weight: 600;
  font-size: 18px;
  font-family: Chalkduster;
}
.info-text {
  width: 90vw;
  font-style: normal;
  font-weight: 500;
  font-size: 17px;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2; /* number of lines to show */
  line-clamp: 2;
  -webkit-box-orient: vertical;
}

</style>
