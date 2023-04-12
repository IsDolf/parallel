<template>
  <div
    class="sheet-wrapper-wrapper fixed-bottom transparent-black"
    @click="this.$emit('onama-toggle')"
  >
    <div class="px-4 fixed-bottom bg-white sheet-wrapper pb-3">
      <div class="pt-4">
        <p class="free-days-title m-0 p-0 fs-1">O nama</p>
      </div>
      <div class="mt-4 free-days fs-5">
        <p>
          Mi smo <span class="parallelFont">Parallel</span>. Znanje stečeno na
          fakultetu omogućilo nam je da se bavimo instrukcijama iz raznih
          područja. Iskustvo i znanje koje smo tim putem stekli potaknulo nas je
          da proširimo svoju djelatnost te olakšamo učenje većem broju učenika i
          studenata. Tako smo došli na ideju da otvorimo vlastitu školu za
          poduke.
        </p>
        <p>
          Odlučili smo ozbiljno pristupiti ideji te uložiti puno truda i vremena
          kako bi realizirali naš projekt. S vremenom, kao učenici i studenti,
          upoznali smo se s obrazovnim sustavom i njegovim nedostatcima pa ovim
          putem želimo ponuditi pomoć svima onima koji nailaze na razne
          prepreke, na kakve smo i sami nailazili prilikom obrazovnog procesa.
        </p>
        <p>
          Baš zato što smo mladi i osvješteni vjerujemo da možemo prenositi
          znanje na jednostavan i zanimljiv način.
        </p>
        <p>
          Škola Parallel počela je s radom u Rijeci 1. veljače 2022. godine.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  emits: ['onama-toggle'],
  data() {
    return {
    };
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
</style>
