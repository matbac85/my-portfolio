<template>
  <section>
    <h2 class="title">
      My<br /><strong class="strong-title-item">Works</strong>
    </h2>
    <ul>
      <Work v-for="(work, index) in works" :key="index" :skill="skill" />
    </ul>
  </section>
</template>

<script setup></script>

<style scoped></style>
