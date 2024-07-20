<template>
  <nav>
    <img loading="lazy" src="/images/logo.svg" alt="" class="logo" />
    <img class="burger-menu" src="/images/burger-menu.svg" alt="" />
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#works">Works</a></li>
      <li><a href="#resume">Resume</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<script setup></script>

<style scoped>
.burger-menu {
  display: none;
}

ul {
  padding: 0;
  display: flex;
  gap: 2rem;
  align-items: center;
}

li {
  all: unset;
}

a {
  text-decoration: none;
  font-family: "Open Sans", sans-serif;
  font-weight: 700;
  color: var(--secondary);
}

a:hover {
  color: var(--accent);
}

nav {
  min-width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: var(--primary);
  height: var(--nav-height);
  padding-inline: clamp(1rem, 3.005vw + 0.296rem, 3rem);
  padding-block: clamp(1rem, 0.751vw + 0.824rem, 1.5rem);
  position: fixed;
  top: 0;
  left: 0;
  z-index: 3;
  box-shadow: 0px 10px 15px -3px rgba(0, 0, 0, 0.2);
}

.logo {
  height: 90%;
}
</style>
