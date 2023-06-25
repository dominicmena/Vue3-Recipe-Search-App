<template>

<div>
    {{ingredients}}
</div>
</template>

<script setup>
import { onMounted } from 'vue';
import axiosClient from '../axiosClient'
import { ref } from 'vue';

const ingredients = ref([])

onMounted(() => {
    axiosClient.get('list.php?i=list').then(({data}) => {
        debugger
        ingredients.value = data
    })
})
</script>