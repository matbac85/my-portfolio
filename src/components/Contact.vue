<template>
  <section>
    <h2 class="title">
      Contact<br /><strong class="strong-title-item">Me</strong>
    </h2>
    <a class="mail" href="mailto:mathildebaclin@gmail.com"
      >mathildebaclin@gmail.com</a
    >
    <div class="socials">
      <a href="https://github.com/matbac85">Github</a
      ><a href="https://www.linkedin.com/in/matbac/">Linkedin</a>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.mail {
  font-family: "Playfair Display", serif;
  font-style: italic;
  color: var(--secondary);
  font-size: 4rem;
  text-decoration: none;
  margin-bottom: 3rem;
  position: relative;
  width: fit-content;
}

.mail::after {
  content: "";
  position: absolute;
  top: 98%;
  left: 0;
  height: 1px;
  background-color: var(--secondary);
  width: 100%;
}

.socials {
  display: flex;
  gap: 2rem;
}

.socials a {
  background-color: var(--accent);
  font-family: "Open Sans", sans-serif;
  font-weight: 700;
  color: var(--primary);
  font-size: 2rem;
  border: 1px solid transparent;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  text-decoration: none;
  font-style: normal;
}

.socials a:hover {
  color: var(--accent);
  border: 1px solid var(--accent);
  background-color: var(--primary);
}
</style>
