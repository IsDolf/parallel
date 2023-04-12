<template>
  <div class="bg-info position-absolute start-0 w-100 h-150">
    <div class="first-section pb-5">
      <NavbarComponent />
      <InfoComponent @onama-toggle="this.onamaPageOpen = !this.onamaPageOpen" />
      <CardsComponent />
      <InfoComponentTwo
        @onama-two-toggle="this.onamaTwoPageOpen = !this.onamaTwoPageOpen"
      />
  </div>
    <OnamaComponent
      v-if="onamaPageOpen"
      @onama-toggle="this.onamaPageOpen = !this.onamaPageOpen"
    />
    <ListaComponent
      v-if="onamaTwoPageOpen"
      @onama-two-toggle="this.onamaTwoPageOpen = !this.onamaTwoPageOpen"
    />
    <div class="bg-info">
      <ContactCardComponent />
      <AccordionComponent />
      <FooterComponent />
    </div>
  </div>
</template>
<script>
export default {
    data() {
        return {
            onamaPageOpen: false,
            onamaTwoPageOpen: false,
        };
    },
};
</script>
<script setup>
import NavbarComponent from "../components/NavbarComponent.vue";
import InfoComponent from "../components/InfoComponent.vue";
import CardsComponent from "../components/CardsComponent.vue";
import ContactCardComponent from "../components/ContactCardComponent.vue";
import AccordionComponent from "../components/AccordionComponent.vue";
import FooterComponent from "../components/FooterComponent.vue";
import { useToast } from "vue-toastification";
import OnamaComponent from "../components/OnamaComponent.vue";
import InfoComponentTwo from "../components/InfoComponentTwo.vue";
import ListaComponent from "../components/ListaComponent.vue";

const toast = useToast();

setTimeout(() => {
  toast(
    "Upisi na pripreme za državnu maturu traju od 1. veljače 2023. do 15. ožujka 2023. Upiši se i rezerviraj svoje mjesto.",
    {
      timeout: 15000,
    }
  );
}, 15000);
</script>

<style scoped>
.first-section {
  background-image: linear-gradient(
    109.6deg,
    rgba(156, 252, 248, 1) 11.2%,
    rgba(110, 123, 251, 1) 91.1%
  );
  box-shadow: rgba(0, 0, 0, 0.4) 0px 2px 4px,
    rgba(0, 0, 0, 0.3) 0px 7px 13px -3px, rgba(0, 0, 0, 0.2) 0px -3px 0px inset;

  border-radius: 0 0 1000em 1000em / 0 0 100em 100em;
  height: auto;
  padding-bottom: 3vw!important;
}
</style>

<style>
h1,
h2 {
  font-family: Chalkduster;
}

p {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  font-size: 20px !important;
}

h3,
h4 {
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
}

button {
  font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}

.parallelFont {
  font-family: Chalkduster;
  font-size: larger;
}
</style>
