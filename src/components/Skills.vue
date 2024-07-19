<template>
  <section>
    <h2 class="title">
      My<br /><strong class="strong-title-item">Skills</strong>
    </h2>
    <ul>
      <Skill v-for="(skill, index) in skills" :key="index" :skill="skill" />
    </ul>
  </section>
</template>

<script setup>
import Skill from "./Skill.vue";

const skills = [
  "HTML",
  "CSS",
  "JS",
  "Vue.js",
  "React",
  "Tailwind",
  "Photoshop",
  "Illustrator",
  "InDesign",
  "Figma",
];
</script>

<style scoped>
ul {
  all: unset;
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
}
</style>
