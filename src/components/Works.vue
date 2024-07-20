<template>
  <section>
    <h2 class="title">
      My<br /><strong class="strong-title-item">Works</strong>
    </h2>
    <ul>
      <WorkCard
        v-for="(work, index) in works"
        :key="index"
        :image="work.img"
        :title="work.title"
        :tags="work.tags"
      />
    </ul>
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
];
</script>

<style scoped>
ul {
  padding: 0;
  display: flex;
  gap: 1.5rem;
  flex-wrap: wrap;
}
</style>
