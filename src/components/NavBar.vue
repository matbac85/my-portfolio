<template>
  <nav>
    <img loading="lazy" src="/images/logo.svg" alt="Logo" class="logo" />
    <button
      class="menu-wrapper"
      @click="openMenu = !openMenu"
      :class="{ active: openMenu }"
    >
      <div class="menu-bar one"></div>
      <div class="menu-bar two"></div>
    </button>
    <ul class="desktop">
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#works">Works</a></li>
      <li><a href="#resume">Resume</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <div class="menu-overlay" v-if="openMenu">
      <ul>
        <li><a href="#home" @click="closeMenu">Home</a></li>
        <li><a href="#about" @click="closeMenu">About</a></li>
        <li><a href="#skills" @click="closeMenu">Skills</a></li>
        <li><a href="#works" @click="closeMenu">Works</a></li>
        <li><a href="#resume" @click="closeMenu">Resume</a></li>
        <li><a href="#contact" @click="closeMenu">Contact</a></li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const openMenu = ref(false);

console.log(openMenu.value);

function closeMenu() {
  openMenu.value = false;
}
</script>

<style scoped>
button {
  all: unset;
  z-index: 1000;
}

.menu-wrapper {
  width: 40px;
  cursor: pointer;
  position: relative;
  height: 100%;
}

.menu-bar {
  position: absolute;
  width: 100%;
  height: 4px;
  background: var(--secondary);
  left: 0%;
}

.one {
  top: 10px;
  animation-delay: 0.1s;
  transition: all 0.3s;
}

.two {
  top: 18px;
  transition: all 0.3s;
}

@keyframes slideOut {
  0% {
    width: 100%;
    left: 0%;
    right: auto;
  }

  50% {
    width: 0%;
    left: 0%;
    right: auto;
  }
  51% {
    width: 0%;
    right: 0%;
    left: auto;
  }

  100% {
    width: 100%;
    right: 0%;
    left: auto;
  }
}

.menu-wrapper:hover .menu-bar.active {
  animation: none;
}
.active .one {
  top: 50%;
  left: 0%;
  transform: rotate(45deg);
}
.active .two {
  top: 50%;
  left: 0%;
  transform: rotate(-45deg);
}

.menu-overlay ul {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  text-align: center;
  padding: 0;
}

.menu-overlay li {
  all: unset;
}

.menu-overlay a {
  text-decoration: none;
  font-family: "Playfair Display", serif;
  font-weight: 400;
  color: var(--secondary);
  font-size: 3rem;
  text-align: center;
}

.menu-overlay a:hover {
  color: var(--accent);
}

.menu-overlay {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: var(--primary);
  color: var(--secondary);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 100;
  overflow: hidden;
  padding: 0;
  transition: opacity 0.3s ease, visibility 0.3s ease;
}

.menu-overlay.active {
  display: flex;
  opacity: 1;
  visibility: visible;
}

.desktop {
  display: none;
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

@media (min-width: 48rem) {
  .menu-wrapper {
    display: none;
  }

  .menu-overlay {
    display: none;
  }

  .desktop {
    padding: 0;
    display: flex;
    gap: 2rem;
    align-items: center;
  }
}

@media (min-width: 100rem) {
  nav {
    padding-inline: 6rem;
    font-size: 1.5rem;
  }

  nav ul {
    gap: 2.5rem;
  }
}
</style>
