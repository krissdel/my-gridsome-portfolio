<template>
  <section id="contact" class="contact-section">
    <v-container>
      <v-row>
        <v-col>
          <h1 class="text-center">Contact information</h1>
        </v-col>
      </v-row>
      <v-row>
        <v-col sm="6" offset-sm="3" class="d-flex justify-space-around">
          <v-icon> </v-icon>
         
          <img
            class="contact-icon"
            src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg"
            :href="contact.github"
          />
          <img
            class="contact-icon"
            src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg"
          />
          <img
            class="contact-icon"
            src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/twitter.svg"
          />
          <img
            class="contact-icon"
            src="https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/instagram.svg"
          />
          
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>



<script>
export default {
  data() {
    return {
      contact: [
        {
          github: "https://github.com/krissdel",
        },
      ],
    };
  },
};
</script>



<style scoped>
h1 {
  color: white;
}
.contact-section {
  background-color: #003a53;
}
.contact-icon {
  height: 30px;
}
</style>