<script setup>
const route = useRoute()

const { data } = useFetch(`https://rickandmortyapi.com/api/character?page=${route.params.id}`, {
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