<script setup>
const { data } = defineProps(['data'])
</script>

<template>
  <div class="card">
    <img :src="data.image" class="card-img-top" :alt="data.name" />
    <div class="card-body d-grid">
      <h5 class="card-title">{{ data.name }}</h5>
      <p>Appare in <strong>{{ data.episode.length }}</strong> episodi</p>
      <NuxtLink :to="`/character/${data.id}`" class="btn btn-primary">
        Vedi dettaglio
      </NuxtLink>
    </div>
  </div>
</template>

<style lang="scss" scoped>
img {
  min-height: 300px;
  background-color: lightgray;
}
</style>