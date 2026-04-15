<script setup>
import MenuComponent from './components/menu-component.vue'
import HomePage from './views/home-page.vue'
</script>

<template>
  <MenuComponent />
  <main>
    <HomePage />
  </main>
</template>

<style scoped>
* {
  font-family: 'Inter', sans-serif;
}
main {
  background: var(--color-background);
}
</style>
