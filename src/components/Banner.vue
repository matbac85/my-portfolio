<template>
  <section id="home">
    <h1 class="sr-only">Le portfolio de Mathilde Baclin</h1>
    <p class="animated-text">
      Creating <strong>Elegant</strong> Web Experiences
    </p>
  </section>
</template>

<script setup></script>

<style scoped>
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}

section {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 0;
  overflow-x: hidden;
}

p {
  font-family: "Playfair Display", serif;
  font-size: clamp(4rem, 6.009vw + 2.592rem, 8rem);
  color: var(--secondary);
  line-height: 120%;
  max-width: 62rem;
  text-align: center;
  opacity: 0;
  transform: translateX(100%);
  animation: slideInFromRight 2s forwards;
}

strong {
  color: var(--accent);
  font-style: italic;
  font-weight: 400;
}

@keyframes slideInFromRight {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>
