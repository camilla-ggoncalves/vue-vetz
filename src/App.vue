<script setup>
import NavComponent from '../src/components/NavComponent.vue';
</script>

<template>
  <NavComponent></NavComponent>

  <router-link to="/home">Homepage</router-link>
  <router-link to="/about">Sobre Nós</router-link>

  <router-view /> <!-- Para aparecer o conteúdo das páginas -->
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
</style>
