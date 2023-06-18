<template>
{{meals}}

</template>

<script setup>
import { computed } from 'vue';
import store from '../src/store/index';


const meals = computed(() => store.state.meals)

</script>