<template>
  <div
    class="rounded-4 rounded-start py-2 mt-4 special-box-shadow info-tab"
    @click="this.$emit('onama-toggle')"
  >
    <p class="mx-3 my-1 info-title">O nama</p>
    <p class="mx-3 my-1 info-text">
      Mi smo <span class="parallelFont">Parallel</span>. Znanje stečeno na
      fakultetu omogućilo nam je da se bavimo instrukcijama iz raznih područja.
      Iskustvo i znanje koje smo tim putem stekli potaknulo nas je da proširimo
      svoju djelatnost te olakšamo učenje većem broju učenika i studenata. Tako
      smo došli na ideju da otvorimo vlastitu školu za poduke. Odlučili smo
      ozbiljno pristupiti ideji te uložiti puno truda i vremena kako bi
      realizirali naš projekt. S vremenom, kao učenici i studenti, upoznali smo
      se s obrazovnim sustavom i njegovim nedostatcima pa ovim putem želimo
      ponuditi pomoć svima onima koji nailaze na razne prepreke, na kakve smo i
      sami nailazili prilikom obrazovnog procesa. Baš zato što smo mladi i
      osvješteni vjerujemo da možemo prenositi znanje na jednostavan i zanimljiv
      način.
    </p>
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
