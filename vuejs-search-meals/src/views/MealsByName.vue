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

  <div class="grid grid-cols-1 md:grid-cols-3 gap-5 p-8">
    <div
      v-for="meal of meals"
      :key="meal.idMeal"
      class="bg-white shadow rounded-xl"
    >
      <img
        :src="meal.strMealThumb"
        alt="strMeal"
        class="rounded-t-xl h-48 w-full object-cover"
      />
      <div class="p-3">
        <h3 class="font-bold">{{ meal.strMeal }}</h3>
        <p class="mb-4">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolorum
          dolor asperiores excepturi?
        </p>
        <div>
          <a
            :href="meal.strYoutube"
            target="_blank"
            class="px-3 py-2 rounded border-red-600 bg-red-500 text-white hover:bg-white hover:text-black transition-colors"
            >Youtube</a
          >
          <router-link to="/" class=" ml-2 px-3 py-2 rounded border-red-600 bg-red-500 text-white hover:bg-white hover:text-black transition-colors"> View </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { computed } from "@vue/reactivity";
import { ref } from "vue";
import store from "../store";

const keyword = ref("");
const meals = computed(() => store.state.searchedMeals);

function searchMeals() {
  store.dispatch("searchMeals", keyword.value);
}
</script>
