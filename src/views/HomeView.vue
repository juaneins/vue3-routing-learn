<script setup>
import cars from '../data/cars.json';
import { RouterLink } from 'vue-router';
</script>

<template>
  <div>
    <h1>Home View</h1>
    <div class="cars">
      <RouterLink v-for="car in cars" :key="car.id" :to="`/cars/${car.id}`">
        {{ car.name }}
      </RouterLink>
    </div>
  </div>
</template>
