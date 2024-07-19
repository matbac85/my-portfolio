<template>
  <li>
    <img src="../assets/Images/bullet.svg" alt="" />
    <div class="content">
      <h3>{{ position }}</h3>
      <p class="context">{{ context }}</p>
      <p class="description">{{ description }}</p>
    </div>
  </li>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  position: String,
  context: String,
  description: String,
});
</script>

<style scoped>
li {
  all: unset;
  display: flex;
  flex-direction: row;
  align-items: start;
  gap: 2rem;
  position: relative;
  padding-bottom: 2rem;
}

li:last-child {
  padding-bottom: 0;
}

img {
  width: 2.5rem;
  z-index: 1;
}

li::after {
  content: "";
  position: absolute;
  left: 1.25rem; /* Position it in the middle of the image */
  top: 2.5rem;
  bottom: 0;
  width: 1px;
  background-color: var(--secondary);
  z-index: 2;
}

h3 {
  color: var(--accent);
  font-weight: 300;
  font-size: 2rem;
  text-transform: uppercase;
  letter-spacing: 5px;
  margin-bottom: 4px;
  line-height: 100%;
}

.context {
  font-weight: 700;
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
}
</style>
