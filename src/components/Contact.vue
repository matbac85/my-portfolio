<template>
  <section id="contact">
    <h2 class="title">
      Contact<br /><strong class="strong-title-item">Me</strong>
    </h2>
    <a class="mail" href="mailto:mathildebaclin@gmail.com"
      >mathildebaclin@gmail.com</a
    >
    <div class="socials">
      <a href="https://github.com/matbac85" target="_blank">Github</a
      ><a href="https://www.linkedin.com/in/matbac/" target="_blank"
        >Linkedin</a
      >
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.title {
  margin-top: 0;
}
.mail {
  font-family: "Playfair Display", serif;
  font-style: italic;
  color: var(--accent);
  font-size: clamp(1.5rem, 2.254vw + 0.972rem, 3rem);
  text-decoration: none;
  margin-bottom: clamp(2rem, 1.502vw + 1.648rem, 3rem);
  position: relative;
  width: fit-content;
}

.mail::after {
  content: "";
  position: absolute;
  top: 98%;
  left: 0;
  height: 5px;
  background-color: var(--accent);
  width: 100%;
  cursor: pointer;
}

.mail:hover {
  color: var(--secondary);
}

.mail:hover::after {
  background-color: var(--secondary);
}

.socials {
  display: flex;
  gap: clamp(1.5rem, 0.751vw + 1.324rem, 2rem);
}

.socials a {
  background-color: var(--accent);
  font-family: "Open Sans", sans-serif;
  font-weight: 700;
  color: var(--primary);
  font-size: 1rem;
  border: 1px solid transparent;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  text-decoration: none;
  font-style: normal;
  cursor: pointer;
}

.socials a:hover {
  color: var(--accent);
  border: 1px solid var(--accent);
  background-color: var(--primary);
}

@media (min-width: 105rem) {
  .socials a {
    font-size: 1.5rem;
    padding: 1.25rem 2rem;
  }

  .mail {
    font-size: 4rem;
    margin-bottom: 4rem;
  }
}
</style>
