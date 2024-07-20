<template>
  <article>
    <img :src="image" alt="" />
    <div class="text-content">
      <h3>{{ title }}</h3>
      <ul>
        <li v-for="(tag, index) in tags" :key="index">{{ tag }}</li>
      </ul>
    </div>
  </article>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  image: String,
  title: String,
  tags: Array,
});
</script>

<style scoped>
article {
  border: 1px var(--secondary) solid;
  width: 22rem;
  border-radius: 0.5rem;
  padding: 1rem;
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
  line-height: 100%;
  margin-bottom: 1rem;
}

ul {
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
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
</style>
