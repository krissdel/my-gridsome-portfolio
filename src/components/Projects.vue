<template>
  <section id="projects" class="project-section">
    <v-container>
      <v-row>
        <v-col>
          <h1>Projects</h1>
        </v-col>
      </v-row>
      
      <v-row class="justify-space-around mb-8 mt-4;">
        <!-- =================================== -->

        <!-- ========================================== -->
      
        <v-card
        
          v-for="project in project"
          :key="project.name"
          class="mb-5"
          max-width="300"
        >
        
          <v-img
            class="orange--text align-end"
            height="250px"
            :src="project.image"
            
          >
          </v-img>
          

          <v-card-text class="text--primary">
            <v-card-title class="blue-grey-darken--text align-end"
              >{{ project.name }}
            </v-card-title>
            {{ truncate(project.description) }}
          </v-card-text>

          <v-card-actions>
            <v-btn color="orange" text :href="project.github">
              Github Repo
            </v-btn>
          </v-card-actions>
        </v-card>
         
     
     




      </v-row>
    </v-container>
  </section>
</template>


<script>
import { METHODS } from "http";
export default {
  data() {
    return {
      project: [
        {
          name: "Groupomania",
          github: "https://github.com/krissdel/groupomania",
          description: "Réseau social d'entreprise",
          image: require("./images/groupomania_projet.png"),
        },
        {
          name: "So pekocko (piquante)",
          github: "https://github.com/krissdel/projet-6",
          description: "API sauces piquante",
          image: require("./images/so-pekocko.png"),
        },
        {
          name: "Orinoco",
          github: "https://github.com/krissdel/orinoco-website",
          description: "Site e-commerce (version P.O.O)",
          image: require("./images/orinoco.png"),
        },
        {
          name: "La chouette agence",
          github: "https://github.com/krissdel/chouetteafter",
          description: "Optimisation de site web (SEO)",
          image: require("./images/chouette_agence.png"),
        },
        {
          name: "Ohmyfood",
          github: "https://github.com/krissdel/ohmyfood",
          description: "Dynamiser une page web (animations CSS)",
          image: require("./images/ohmyfood.png"),
        },
        {
          name: "Projet CV",
          github: "https://github.com/krissdel/CV4",
          description: "Transformer une maquette en site web ",
          image: require("./images/cv.png"),
        },
      ],
    };
  },
  methods: {
    truncate(str) {
      if (str.length > 80) {
        return str.slice(0, 79) + "...";
      }
      return str;
    },
  },
};
</script>

<style scoped>
.project-section {
  background-color: #003a53;
}
h1 {
  color: white;
}

/* .v-image {  */
/* filter: grayscale(100%); 

opacity: .5; 
 border: 1px ;  */

/* } */
</style>