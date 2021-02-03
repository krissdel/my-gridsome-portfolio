<template>
  <section id="education-experience">
    <v-container>
      <v-row>
        <v-col>
          <h1>Education</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-timeline>
            <v-timeline-item
              v-for="(year, i) in years"
              :key="i"
              :color="year.color"
              small
            >
              <template v-slot:opposite>
                <span
                  :class="`headline font-weight-bold ${year.color}--text`"
                  v-text="year.year"
                ></span>
              </template>

              <div class="py-4">
                <h2
                  :class="`headline font-weight-light mb-4 ${year.color}--text`"
                >
                  <span v-text="year.title"></span>
                </h2>
                <div>
                  <span v-text="year.text"></span>
                </div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>


<script>
export default {
  data: () => ({
    years: [
      {
        color: "#78909C",
        year: "2020",
        title: "Openclassrooms",
        text: "Développement web, technique et numérique",
      },
      {
        color: "#455A64",
        year: "2006",
        title: "Licence PPL (avion)",
        text: "ACPN (aéroclub)",
      },
      {
        color: "#37474F",
        year: "1998",
        title: "Deug Biochimie",
        text: "Université Cergy Pontoise",
      },
      {
        color: "#003a53",
        year: "1995",
        title: "Bac biochimie Genie Biologie",
        text: "Lycée (Quimper)",
      },
    ],
  }),
};
</script>