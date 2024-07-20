<template>
  <section id="works">
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
          :code="work.code"
          :site="work.site"
          ref="workCards"
        />
      </ul>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import WorkCard from "./WorkCard.vue";

const works = [
  {
    img: "./images/nest.png",
    title: "nest",
    tags: ["Figma", "Vue.js", "Tailwind", "RESTful API", "Responsive"],
    code: "https://github.com/matbac85/nest-app",
    site: "https://nest.mathildebaclin.com/",
  },
  {
    img: "./images/clock.png",
    title: "clock app",
    tags: ["HTML", "CSS", "JS", "RESTful API", "Responsive"],
    code: "https://github.com/matbac85/clock-app",
    site: "https://matbac85.github.io/clock-app/",
  },
  {
    img: "./images/splitter.png",
    title: "tip calculator",
    tags: ["Vue.js", "CSS", "Responsive"],
    code: "https://github.com/matbac85/tip-calculator-app",
    site: "https://matbac85.github.io/tip-calculator-app/",
  },
  {
    img: "./images/advice.png",
    title: "advice generator",
    tags: ["HTML", "CSS", "JS", "RESTful API", "Responsive"],
    code: "https://github.com/matbac85/advice-generator-app",
    site: "https://matbac85.github.io/advice-generator-app/",
  },
  {
    img: "./images/password.png",
    title: "password generator",
    tags: ["Vue.js", "CSS", "Responsive"],
    code: "https://github.com/matbac85/password-generator-app",
    site: "https://matbac85.github.io/password-generator-app/",
  },
  {
    img: "./images/landing-page.png",
    title: "landing page",
    tags: ["HTML", "CSS", "Responsive"],
    code: "https://github.com/matbac85/workit-landing-page",
    site: "https://matbac85.github.io/workit-landing-page/",
  },
  {
    img: "./images/calculator.png",
    title: "age calculator",
    tags: ["Vue.js", "Tailwind", "Responsive"],
    code: "https://github.com/matbac85/AgeCalculatorApp",
    site: "https://matbac85.github.io/AgeCalculatorApp/",
  },
  {
    img: "./images/bmi-calculator.png",
    title: "bmi calculator",
    tags: ["Vue.js", "CSS", "Responsive"],
    code: "https://github.com/matbac85/BmiCalculator",
    site: "https://matbac85.github.io/BmiCalculator/",
  },
  {
    img: "./images/nestor.png",
    title: "nestor's soaps",
    tags: ["Illustrator", "Photoshop", "InDesign"],
    site: "https://www.behance.net/gallery/177027903/Les-savons-de-Nestor-Cration-complete-pour-une-marque",
  },
];

const workCards = ref([]);

const handleScroll = () => {
  const revealPoint = window.innerHeight * 0.85;

  workCards.value.forEach((card, index) => {
    const cardTop = card.getBoundingClientRect().top;

    if (cardTop < revealPoint) {
      card.classList.add("show");
    }
  });
};

onMounted(() => {
  workCards.value = document.querySelectorAll(".work-card");
  window.addEventListener("scroll", handleScroll);
  handleScroll();
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", handleScroll);
});
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
