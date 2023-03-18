<script setup>
const route = useRoute()

const { data } = useFetch(`https://rickandmortyapi.com/api/character/${route.params.id}`, {
  default: () => ({
    name: "",
    image: ""
  })
})
</script>

<template>
  <NuxtLayout name="main">
    <h1>{{ data.name }}</h1>
    <img :src="data.image" :alt="data.name" class="img-thumbnail" />

    <section>
      <NuxtLink to="/" class="btn btn-primary">
        Torna indietro
      </NuxtLink>
    </section>

  </NuxtLayout>
</template>