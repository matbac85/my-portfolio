<template>
  <section id="about">
    <h2 class="title">
      My name is <br /><strong class="strong-title-item">Mathilde</strong>
    </h2>
    <div class="description">
      <p>I’m a junior web developer with a knack for design.</p>
      <p>
        With a strong foundation in frontend development and a background in
        prepress design and production management, I specialize in crafting
        visually appealing and user-friendly websites.
      </p>
      <p>
        I'm eager to collaborate on innovative projects that marry form and
        function seamlessly.
      </p>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.description {
  font-family: "Open Sans", sans-serif;
  color: var(--secondary);
  font-size: 1.25rem;
  line-height: 130%;
  max-width: clamp(30rem, 25vw + 7.5rem, 37.5rem);
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

@media (min-width: 95rem) {
  .description {
    font-size: 2rem;
  }
}
</style>
