<script setup>

const { data } = useFetch('https://rickandmortyapi.com/api/character', {
  default: () => ({ results: [] })
} )

</script>

<template>
  <NuxtLayout name="main">
    <ul class="list-unstyled">
      <li v-for="item in data.results" :key="item.id">
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
    transition: all 0.2s ease-out;
    transform: scale(0.9);

    &:hover {
      transform: scale(1);
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    }
  }
}
</style>