<template>
  <Layout>
    <section>
      <v-container>
         <v-row>
            <v-col>
                <g-image alt="ma photo de profile" src="~/moi.png" width="300" />
                
            </v-col>
            <v-col>
              <!-- <div class="d-flex flex-column"> -->

                <h1>Hi!  </h1>
                <h2>i'm christ</h2>
                <p> i'm a full stack dev </p>
                <!-- </div> -->
            </v-col>
         </v-row>
      </v-container>  
</section>

   
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Hello, world!",
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
