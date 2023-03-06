<script setup>
const route = useRoute()

const episode = ref({})

onMounted(async () => {
  const response = await fetch(`https://rickandmortyapi.com/api/episode/${route.params.id}`)
  const json = await response.json()
  episode.value = json
})

</script>

<template>
  <NuxtLayout name="main">
    <h1>{{ episode.name }}</h1>
    <p>{{ episode.air_date }}</p>
    <p>{{ episode.episode }}</p>
    <p>{{ episode.characters }}</p>
  </NuxtLayout>
</template>