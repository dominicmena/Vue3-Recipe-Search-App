<template>
  <div class="bg-white shadow rounded-xl hover:scale-105 transition-all">
    <router-link :to="{ name: 'mealDetails', params: { id: meal.idMeal } }">
      <img
        :src="meal.strMealThumb"
        alt="meal.strMeal"
        class="rounded-t-xl h-48 w-full object-cover"
      />
    </router-link>
    <div class="p-3">
      <h3 class="font-bold">{{ meal.strMeal }}</h3>
      <h4 class="">{{ meal.strCategory }}</h4>
      <p class="mb-4">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolorum dolor
        asperiores excepturi?
      </p>
      <div>
        <YouTubeButton :href="meal.strYoutube">Youtube</YouTubeButton>
      </div>
    </div>
  </div>
</template>

<script setup>
import YouTubeButton from './YouTubeButton.vue';
const { meal } = defineProps({
  meal: Object,
});
</script>
