<template>
    <a
            :href="href"
            target="_blank"
            class="px-3 py-2 rounded border-red-600 bg-red-500 text-white hover:bg-white hover:text-black transition-colors"
            ><slot></slot></a
          >
</template>

<script setup>
const props = defineProps({
    href: String
})

</script>