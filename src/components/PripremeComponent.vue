<template>

        <ul class="list-group list-group-flush p-3 rounded-5 shadow m-1 bg-white mx-1 my-5">
          <li
            class="list-group-item h4 d-flex justify-content-between"
            v-for="program in programiPriprema"
            :class="{ activated: program.isActive }"
            @click="editTest(program)"
          >
          <div>
            <span class="w-100">{{ program.ime }} </span
            ><span class="text-muted d-flex justify-content-start">{{
              program.brojSati
            }}</span></div>
            <span class="fs-5 d-flex justify-content-end align-items-end overflow-visible word-wrap"
               >{{ program.cijena }} EUR <!-- ({{
                (Math.round(program.cijena * 7.5345 * 100) / 100).toFixed(2)
              }}
              kn)--></span 
            >
          </li>
          <div
            class="card-header d-flex justify-content-center display-5 m-2 rounded-4"
          >
            Ubrzani programi priprema
          </div>
          <li
            class="list-group-item h4 d-flex justify-content-between"
            v-for="program in ubrzaniProgramiPriprema"
            :class="{ activated: program.isActive }"
            @click="editTest(program)"
          >
          <div>
            <span class="w-100">{{ program.ime }} </span
            ><span class="text-muted d-flex justify-content-start">{{
              program.brojSati
            }}</span></div>
            <span class="fs-5 d-flex justify-content-end align-items-end overflow-visible word-wrap"
               >{{ program.cijena }} EUR <!-- ({{
                (Math.round(program.cijena * 7.5345 * 100) / 100).toFixed(2)
              }}
              kn)--></span 
            >
          </li>
          <div class="h3 d-flex justify-content-center text-center fw-bold">
            Iznos: {{ iznos }} EUR ({{
              (Math.round(iznos * 7.5345 * 100) / 100).toFixed(2)
            }}
            kn)
          </div>
        </ul>
        <p class="h6 mx-5 text-center">
          Fiksni tečaj konverzije 1 EUR = 7,53450 kn.
        </p>
        <p class="h5 mx-5 text-center">
          Izvedbeni program priprema za državnu maturu je osmišljen u skladu sa
          službenim ispitnim katalozima koje izdaje Nacionalni centar za vanjsko
          vrednovanje obrazovanja.
        </p>

</template>

<script>
export default {
  data() {
    return {
      activated: false,
      iznos: 0,

      programiPriprema: [
        {
          ime: "Matematika A razina",
          brojSati: "70 školskih sati",
          cijena: 390,
          isActive: false,
        },
        {
          ime: "Matematika B razina",
          brojSati: "50 školskih sati",
          cijena: 280,
          isActive: false,
        },
        {
          ime: "Engleski jezik A razina",
          brojSati: "40 školskih sati",
          cijena: 240,
          isActive: false,
        },
        {
          ime: "Engleski jezik B razina",
          brojSati: "30 školskih sati",
          cijena: 180,
          isActive: false,
        },
        {
          ime: "Hrvatski",
          brojSati: "60 školskih sati",
          cijena: 340,
          isActive: false,
        },
        {
          ime: "Fizika",
          brojSati: "60 školskih sati",
          cijena: 340,
          isActive: false,
        },
        {
          ime: "Kemija",
          brojSati: "60 školskih sati",
          cijena: 340,
          isActive: false,
        },
      ],
      ubrzaniProgramiPriprema: [
        {
          ime: "Matematika A razina",
          brojSati: "35 školskih sati",
          cijena: 200,
          isActive: false,
        },
        {
          ime: "Fizika",
          brojSati: "30 školskih sati",
          cijena: 180,
          isActive: false,
        },
        {
          ime: "Kemija",
          brojSati: "30 školskih sati",
          cijena: 180,
          isActive: false,
        },
      ],
    };
  },
  methods: {
    editTest(program) {
      if (program.isActive) {
        program.isActive = false;
        this.iznos = this.iznos - program.cijena;
      } else {
        program.isActive = true;
        this.iznos = this.iznos + program.cijena;
      }
    },
  },
  computed: {},
  updated() {},
};
</script>

<style>

.word-wrap {
  white-space: nowrap;
}

.pripreme {
  width: 100vw;
  min-width: 1050px;
}

.list-group-item:hover {
  border-radius: 10px;
  font-style: italic;
  cursor: pointer;
  margin-inline: 4px;
  background-color: rgb(241, 241, 241);
}

.list-group-item {
  border-radius: 6px;
  font-style: italic;
  cursor: pointer;
  margin-inline: 2px;
  background-color: rgb(247, 247, 247);
}

.boxed {
  box-shadow: rgba(50, 50, 93, 0.25) 0px 30px 60px -12px inset,
    rgba(0, 0, 0, 0.3) 0px 18px 36px -18px inset;
}

.activated {
  background-color: rgb(181, 244, 181);
}

.activated:hover {
  background-color: rgb(217, 255, 217);
}

.hoverbutton:hover {
  background-color: lightgreen;
}
</style>
