<script setup>

const data = ref([])

onMounted(async () => {
  const response = await fetch('https://rickandmortyapi.com/api/episode')
  const json = await response.json()
  data.value = json.results
})

</script>

<template>
  <NuxtLayout name="main">
    <ul>
      <li v-for="item in data" :key="item.id">
        <NuxtLink :to="`/episodes/${item.id}`">
          {{ item.name }}
        </NuxtLink>
      </li>
    </ul>
  </NuxtLayout>
</template>