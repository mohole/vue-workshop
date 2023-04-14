<script setup>
const { data } = defineProps(['data'])
</script>

<template>
  <article class="card">
    <NuxtLink :to="`/character/${data.id}`">
      <img :src="data.image" class="card-img-top" :alt="data.name" />
    </NuxtLink>
    <div class="card-body d-grid">
      <h5 class="card-title">{{ data.name }}</h5>
      <p>Appare in <strong>{{ data.episode.length }}</strong> episodi</p>
      <NuxtLink :to="`/character/${data.id}`" class="btn btn-primary">
        Vedi dettaglio
      </NuxtLink>
    </div>
  </article>
</template>

<style lang="scss" scoped>
article {
  img {
    min-height: 300px;
    background-color: lightgray;
  }
}
</style>