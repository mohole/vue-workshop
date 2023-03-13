<script setup>

const data = ref([])

onMounted(async () => {
  const response = await fetch('https://rickandmortyapi.com/api/character')
  const json = await response.json()
  data.value = json.results
})

</script>

<template>
  <NuxtLayout name="main">
    <ul class="list-unstyled">
      <li v-for="item in data" :key="item.id">
        <Card :data="item" />
      </li>
    </ul>
  </NuxtLayout>
</template>

<style lang="scss" scoped>
ul {
  display: grid;
  grid-template-columns: repeat(4, 1fr);

  gap: 20px;

  li {
    cursor: pointer;
    transition: all 0.3s ease;
    transform: scale(0.9);

    &:hover {
      transform: scale(1);
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    }
  }
}
</style>