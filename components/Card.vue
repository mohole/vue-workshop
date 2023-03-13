<script setup>
const { data } = defineProps(['data'])
</script>

<template>
  <div class="card">
    <img :src="data.image" class="card-img-top" :alt="data.name" />
    <div class="card-body">
      <h5 class="card-title">{{ data.name }}</h5>
      <NuxtLink :to="`/character/${data.id}`" class="btn btn-primary btn-block">
        Vedi dettaglio
      </NuxtLink>
    </div>
  </div>
</template>