<script setup>
const props = defineProps(['results'])
</script>

<template>
  <ul class="list-unstyled">
    <li v-for="item in props.results" :key="item.id">
      <Card :data="item" />
    </li>
  </ul>
</template>

<style lang="scss" scoped>
ul {
  display: grid;
  grid-template-columns: repeat(1, 1fr);

  gap: 30px;

  li {
    cursor: pointer;
    transition: all 0.2s ease-out;

    &:hover {
      transform: scale(1.1);
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    }
  }
}

@media (min-width: 768px) {
  ul {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 992px) {
  ul {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 1200px) {
  ul {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>