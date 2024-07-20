<template>
  <div>
    <NavBar />
    <main>
      <Banner />
      <Intro />
      <Skills />
      <Works />
      <WorkExperience />
      <Contact />
    </main>
  </div>
</template>

<script setup>
import NavBar from "./components/NavBar.vue";
import Banner from "./components/Banner.vue";
import Intro from "./components/Intro.vue";
import Skills from "./components/Skills.vue";
import Works from "./components/Works.vue";
import WorkExperience from "./components/WorkExperience.vue";
import Contact from "./components/Contact.vue";
</script>

<style scoped>
main {
  height: 100dvh;
}
</style>
