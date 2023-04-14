<script setup>
const route = useRoute()

const { data } = useFetch(`https://rickandmortyapi.com/api/character/${route.params.id}`, {
  default: () => ({
    name: "",
    image: "",
    episode: [],
    status: "",
    location: {
      name: ""
    }
  })
})

const isDead = (status) => status.toLowerCase() === 'dead'

const badgeColor = (status) => [
  'badge',
  isDead(status) ? 'text-bg-danger' : 'text-bg-success'
].join(' ')
</script>

<template>
  <NuxtLayout name="main">
    <section class="data">
      <h1>{{ data.name }}</h1>

      <img :src="data.image" :alt="data.name" class="img-thumbnail" />

      <ul>
        <li>Appare in <strong>{{ data.episode.length }}</strong> episodi</li>
        <li>Status: <span :class="badgeColor(data.status)">{{ isDead(data.status) ? 'morto' : 'vivo' }}</span></li>
        <li>Luogo: <i>{{ data.location.name }}</i></li>
      </ul>
    </section>

    <section class="actions">
      <NuxtLink to="/" class="btn btn-primary btn-lg">
        Torna indietro
      </NuxtLink>
    </section>

  </NuxtLayout>
</template>

<style lang="scss" scoped>
$spacing: 30px;

h1 {
  margin-bottom: $spacing
}

section.data {
  max-width: 500px;
  display: flex;
  gap: $spacing;
  flex-direction: column;

  li {
    font-size: 1.5em
  }
}

section.actions {
  margin-top: $spacing
}
</style>