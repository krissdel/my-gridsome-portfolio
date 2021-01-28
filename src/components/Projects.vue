<template>
  <section class="project-section">
    <v-container>
      <v-row>
        <v-col>
          <h1>Projects</h1>
        </v-col>
      </v-row>
      <v-row class="justify-space-around mb-8 mt-4">

          <v-card 
            v-for="project in project"
            :key="project.name"
          class="" max-width="300">
            <v-img
              class="white--text align-end"
              height="200px"
              src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
            >
            <!-- :src="project.description" -->
              <v-card-title>{{ project.name }} </v-card-title>
            </v-img>

            <v-card-text class="text--primary">
              {{ truncate(project.description) }}
            </v-card-text>

            <v-card-actions>
              <v-btn color="orange" text :href="project.github"> Github Repo </v-btn>

            </v-card-actions>
          </v-card>
        
      </v-row>
    </v-container>
  </section>
</template>


<script>
import { METHODS } from 'http'
export default {
    data() {
        return {
            project: [
                {
                   name: 'Curriculum',
                   github: 'https://github.com/krissdel',
                   description: "",
                   image: ""
                },
                {
                    name: 'Hour Tracking App',
                    github: 'https://github.com/krissdel',
                     description: "",
                   image: ""
                }
            ]
        }
    },
    methods: {
        truncate(str){
            if (str.length > 80){
                            return str.slice(0, 79) + '...'
                        }
               return  str  
                     
               
        }
    }
    
}
</script>

<style scoped>
.project-section {
  background-color: #a6e1fa;
}
/* .v-image { */
    /* filter: grayscale(100%); */
     
     /* opacity: .5; */
     /* border: 1px ; */
/* } */
</style>