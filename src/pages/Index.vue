<template>
  <Layout>
    <About />
    <Projects />
    
    <Education />
    <Contact />
  </Layout>
</template>

<script>
import About from "@/components/About.vue";
import Projects from "@/components/Projects.vue";
import Contact from "@/components/Contact.vue";
import Education from "@/components/Education.vue";

export default {
  metaInfo: {
    title: "Hello, world!",
  },
  components: {
    About,
    Projects,
    Contact,
    Education,
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
