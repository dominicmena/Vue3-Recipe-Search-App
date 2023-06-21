<template>

<div class="p-8">
   <input
   type="text"
   v-model="keyword"
   class="rounded border-2 border-gray-200 w-full"
   placeholder="Search for meals"
   @change="searchMeals"
 />
</div>

<div class="grid grid-cols-1 md:grid-cols-3 gap-5">
   <div v-for="meal of meals" :key="meal.idMeal">
      <img :src="meal.strMealThumb" alt="strMeal"/>
      <h3>{{meal.strMeal}}</h3>
   </div>
</div>
</template>

<script setup>
import { computed } from '@vue/reactivity'
import { ref } from 'vue';
import store from '../store'

const keyword = ref('')
const meals = computed(() => store.state.searchedMeals)

function searchMeals() {
   store.dispatch('searchMeals', keyword.value)
}
</script>