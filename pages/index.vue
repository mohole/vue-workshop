<script setup>
const { data } = useFetch('https://rickandmortyapi.com/api/character', {
  default: () => ({ results: [], info: {} })
})
</script>

<template>
  <NuxtLayout name="main">
    <div>
      <List :results="data.results" />
      <Pagination :info="data.info" />
    </div>
  </NuxtLayout>
</template>