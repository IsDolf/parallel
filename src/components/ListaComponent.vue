<template>
  <div
    class="sheet-wrapper-wrapper fixed-bottom transparent-black"
    @click="this.$emit('onama-two-toggle')"
  >
    <div class="px-4 fixed-bottom bg-white sheet-wrapper pb-3">
      <div class="pt-4">
        <p class="free-days-title m-0 p-0 fs-1">Popis programa</p>
      </div>
      <div class="mt-4 free-days fs-5">
        <ul class="fs-1">
          <li>Matematika</li>
          <li>Fizika</li>
          <li>Kemija</li>
          <li>Biologija</li>
          <li>Hrvatski jezik</li>
          <li>Engleski jezik</li>
          <li>Informatika</li>
          <li>Povijest</li>
          <li>Geografija</li>
          <li>Tehnička kultura</li>
          <li>Statistika</li>
          <li>Programiranje</li>
          <li>Osnove elektrotehnike</li>
          <li>Računalstvo</li>
          <li>Mjerenja u elektrotehnici</li>
          <li>Uvod u elektroniku</li>
          <li>Elektronika</li>
          <li>Elektrotehnika</li>
          <li>Opća i anorganska kemija</li>
          <li>Organska kemija</li>
          <li>Analitička kemija</li>
          <li>Biokemija</li>
          <li>Fizikalna kemija</li>
          <li>Mikrobiologija</li>
          <li>Stabilnost broda</li>
          <li>Poznavanje broda</li>
          <li>Rukovanje teretom</li>
          <li>Astronomska navigacija</li>
          <li>Terestrička navigacija</li>
          <li>Elektronička navigacija</li>
          <li>Brodski strojevi i uređaji</li>
          <li>Tehnička mehanika</li>
          <li>Tehnički materijali</li>
          <li>Termodinamika</li>
          <li>Hidraulika i pneumatika</li>
          <li>Robotika</li>
          <li>Industrijska automatizacija</li>
          <li>Regulacija i upravljanje</li>
        </ul>
      </div>
    </div>
    </div>
</template>

<script>
export default {
  emits: ["onama-two-toggle"],
  data() {
    return {};
  },
};
</script>

<style scoped>
.transparent-black {
  background: rgb(34, 25, 25);
  background: linear-gradient(
    180deg,
    rgba(34, 25, 25, 0.5284488795518207) 0%,
    rgba(255, 255, 255, 0) 100%
  );
}

.sheet-wrapper-wrapper {
  height: 100vh;
  background-color: transparent;
  z-index: 1032;
}

.sheet-wrapper {
  border-radius: 12px 12px 0 0;
  overflow: scroll;
  height: 90vh;
}

.free-days-title {
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 27px;
  letter-spacing: -0.2px;
  color: var(--component-title-color);
  font-family: Chalkduster;
}

.free-days-subtitle {
  font-style: normal;
  font-weight: 600;
  font-size: 17px;
  line-height: 24px;
  letter-spacing: -0.2px;
  color: var(--component-title-color);
}

.free-days-text p {
  font-style: normal;
  font-weight: 400;
  font-size: 17px;
  line-height: 26px;
  color: var(--component-title-color);
  font-family: Chalkduster;
}

.border-top-transparent {
  background: rgb(255, 255, 255);
  background: linear-gradient(
    0deg,
    rgba(255, 255, 255, 0) 0%,
    rgb(0, 0, 0) 47%
  );
}

ul {
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
}

ul li {
  line-height: 50px;
}
</style>
