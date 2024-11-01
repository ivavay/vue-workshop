<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Counter from './components/Counter.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="50" height="50" />

    <div class="wrapper">

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/hello">Hello</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
  nav a {
    color: blue;
  }
  a {
    margin-right: 8px;
  }
</style>
