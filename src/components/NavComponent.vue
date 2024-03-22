<script setup>
import { RouterLink } from 'vue-router';
</script>
<template>
  <header>
    <div class="wrapper">
      <nav>
        <RouterLink active-class="router-link-exact-active" to="/">Home</RouterLink>
        <RouterLink active-class="router-link-exact-active" to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
</template>
<style scoped>
.router-link-exact-active {
  font-weight: bold;
  font-size: larger;
}
</style>
