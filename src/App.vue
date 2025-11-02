<script setup>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';
// router-view is globally available if router is installed correctly
</script>

<style>
/* Basic styles for the layout */
#app {
  font-family: Georgia, 'Times New Roman', Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  min-height: 100vh;
  /* Use the sticky footer logic from earlier */
  display: flex;
  flex-direction: column;
}

main {
  flex-grow: 1;
  /* Ensure main content pushes the footer down */
  padding: 20px;
}
</style>

<template>
  <div id="app">
    <AppHeader />

    <!-- This is where the HomeView or AboutView will be rendered -->
    <main>
      <router-view />
    </main>

    <AppFooter />
  </div>
</template>