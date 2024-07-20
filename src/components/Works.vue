<template>
  <section>
    <h2 class="title">
      My<br /><strong class="strong-title-item">Works</strong>
    </h2>
    <div class="centered">
      <ul>
        <WorkCard
          v-for="(work, index) in works"
          :key="index"
          :image="work.img"
          :title="work.title"
          :tags="work.tags"
        />
      </ul>
    </div>
  </section>
</template>

<script setup>
import WorkCard from "./WorkCard.vue";

const works = [
  {
    img: "/images/nest.png",
    title: "nest",
    tags: ["Figma", "Vue.js", "Tailwind", "RESTful API", "Responsive"],
  },
  {
    img: "/images/clock.png",
    title: "clock app",
    tags: ["HTML", "CSS", "JS", "RESTful API", "Responsive"],
  },
  {
    img: "/images/splitter.png",
    title: "tip calculator",
    tags: ["Vue.js", "CSS", "Responsive"],
  },
  {
    img: "/images/advice.png",
    title: "advice generator",
    tags: ["HTML", "CSS", "JS", "RESTful API", "Responsive"],
  },
  {
    img: "/images/password.png",
    title: "password generator",
    tags: ["Vue.js", "CSS", "Responsive"],
  },
  {
    img: "/images/landing-page.png",
    title: "landing page",
    tags: ["HTML", "CSS", "Responsive"],
  },
  {
    img: "/images/calculator.png",
    title: "age calculator",
    tags: ["Vue.js", "Tailwind", "Responsive"],
  },
  {
    img: "/images/bmi-calculator.png",
    title: "bmi calculator",
    tags: ["Vue.js", "CSS", "Responsive"],
  },
  {
    img: "/images/nestor.png",
    title: "nestor's soaps",
    tags: ["Illustrator", "Photoshop", "InDesign"],
  },
];
</script>

<style scoped>
ul {
  padding: 0;
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
