<template>
  <nav>
    <img src="../assets/images/logo.svg" alt="" /><img
      src="../assets/images/burger-menu.svg"
      alt=""
    />
  </nav>
</template>

<script setup></script>

<style scoped>
nav {
  min-width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: var(--primary);
  height: var(--nav-height);
  padding-inline: clamp(1rem, 3.005vw + 0.296rem, 3rem);
  position: fixed;
  top: 0;
  left: 0;
  z-index: 3;
  box-shadow: 0px 10px 15px -3px rgba(0, 0, 0, 0.2);
}
</style>
