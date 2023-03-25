<script setup>
const props = defineProps(['info'])

const isDisabled = (value) => `page-item ${!value && 'disabled'}`
const getPage = (str) => str ? str.split('?page=')[1] : ''
</script>

<template>
  <nav aria-label="Page navigation example">
    <ul class="pagination justify-content-center">
      <li :class="isDisabled(info.prev)">
        <NuxtLink class="page-link" :to="`/page/${getPage(info.prev)}`">Pagina precedente</NuxtLink>
      </li>
      <li :class="isDisabled(info.next)">
        <NuxtLink class="page-link" :to="`/page/${getPage(info.next)}`">Pagina successiva</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
nav {
  margin: 40px 0;
}
</style>