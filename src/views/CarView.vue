<script setup>
import { useRoute, useRouter, RouterView } from 'vue-router';
import cars from '../data/cars.json';

const route = useRoute();
const router = useRouter();
const carId = parseInt(route.params.id);

const car = cars.find((car) => car.id === carId);
</script>
<template>
  <div v-if="car">
    <h1>Car View</h1>
    <p>{{ car.name }}</p>
    <p>{{ car.price }}</p>
    <p>{{ car.year }}</p>
    <button @click="router.push(`/cars/${carId}/contact`)">Click for contact</button>
    <RouterView />
  </div>
  <div v-else>Car doesn't exist</div>
</template>
