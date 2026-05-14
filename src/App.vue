<template>
  <div id="app-root">
    <AppHeader />
    <main>
      <HomePage />
    </main>
    <AppFooter />
  </div>
</template>

<script setup>
import AppHeader from './components/AppHeader.vue'
import HomePage from './pages/HomePage.vue'
import AppFooter from './components/AppFooter.vue'
</script>