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
  font-size: 1.5rem;
  border: 1px var(--secondary) solid;
  border-radius: 0.5rem;
  padding: 1.5rem 2rem;
}
</style>
