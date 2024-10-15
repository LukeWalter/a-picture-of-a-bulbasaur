<script setup lang="ts">
import { ref } from 'vue';
const { name = 'bulbasaur' } = defineProps<{ name?: string }>()
// console.log(name)
const lowerCaseName = name.toLowerCase()
// console.log(lowerCaseName)
const capitalizedName = ref(lowerCaseName.charAt(0).toUpperCase() + lowerCaseName.slice(1))
// capitalizedName.value = lowerCaseName.charAt(0).toUpperCase() + lowerCaseName.slice(1)
// console.log(capitalizedName.value)
const link = ref("https://img.pokemondb.net/sprites/scarlet-violet/normal/" + lowerCaseName + ".png")
// link.value = "https://img.pokemondb.net/sprites/scarlet-violet/normal/" + lowerCaseName + ".png"
// console.log(link.value)
</script>

<template>
  <img :src="link" :alt="capitalizedName">    
</template>

<style scoped>

</style>