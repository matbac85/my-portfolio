<template>
  <article class="work-card">
    <img loading="lazy" :src="image" alt="" />
    <div class="text-content">
      <h3>{{ title }}</h3>
      <ul>
        <li v-for="(tag, index) in tags" :key="index">{{ tag }}</li>
      </ul>
      <div class="links">
        <a v-if="code" :href="code" target="_blank">view code</a
        ><a v-if="site" :href="site" target="_blank">preview page</a>
      </div>
    </div>
  </article>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  image: String,
  title: String,
  tags: Array,
  code: String,
  site: String,
});
</script>

<style scoped>
article {
  border: 1px var(--secondary) solid;
  width: clamp(22rem, 90vw - 59rem, 31rem);
  border-radius: 0.5rem;
  padding: 1rem;
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

a {
  background-color: var(--accent);
  font-family: "Open Sans", sans-serif;
  font-weight: 700;
  color: var(--primary);
  font-size: 0.875rem;
  border: 1px solid transparent;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  text-decoration: none;
  font-style: normal;
  text-transform: capitalize;
  cursor: pointer;
}

a:hover {
  color: var(--accent);
  border: 1px solid var(--accent);
  background-color: var(--primary);
}

.links {
  display: flex;
  gap: 1rem;
}

article.show {
  opacity: 1;
  transform: translateY(0);
}

.text-content {
  color: var(--secondary);
  font-family: "Open Sans", sans-serif;
  margin-top: 1rem;
  padding: 0 0.5rem;
}

h3 {
  font-weight: 300;
  font-size: 1.5rem;
  text-transform: uppercase;
  letter-spacing: 5px;
  margin-bottom: 4px;
  line-height: 110%;
  margin-bottom: 1rem;
}

ul {
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1rem;
}

li {
  all: unset;
  font-family: "Open Sans", sans-serif;
  font-weight: 700;
  color: var(--secondary);
  font-size: 0.875rem;
  border: 1px var(--secondary) solid;
  border-radius: 0.5rem;
  padding-inline: 0.5rem;
  padding-block: 0.25rem;
}

img {
  border-radius: 0.5rem;
}

@media (min-width: 111rem) {
  h3 {
    font-size: 2rem;
  }

  li,
  a {
    font-size: 1.5rem;
  }
}
</style>
