<template>
  <li>{{ skill }}</li>
</template>

<script setup>
import { defineProps } from "vue";

const props = defineProps({
  skill: String,
});
</script>

<style scoped>
li {
  all: unset;
  font-family: "Open Sans", sans-serif;
  font-weight: 700;
  color: var(--secondary);
  font-size: clamp(1rem, 0.751vw + 0.824rem, 1.5rem);
  border: 1px var(--secondary) solid;
  border-radius: 0.5rem;
  padding-inline: clamp(1.5rem, 0.751vw + 1.324rem, 2rem);
  padding-block: clamp(1rem, 0.751vw + 0.824rem, 1.5rem);
}

@media (min-width: 95rem) {
  li {
    font-size: 2rem;
    padding-inline: 2.5rem;
    padding-block: 2rem;
  }
}
</style>
