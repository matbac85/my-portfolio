<template>
  <section>
    <p>Creating <strong>Elegant</strong> Web Experiences</p>
  </section>
</template>

<script setup></script>

<style scoped>
section {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 0;
}

p {
  font-family: "Playfair Display", serif;
  font-size: clamp(4rem, 6.009vw + 2.592rem, 8rem);
  color: var(--secondary);
  line-height: 120%;
  max-width: 62rem;
  text-align: center;
}

strong {
  color: var(--accent);
  font-style: italic;
  font-weight: 400;
}
</style>
