<script setup>
const year = new Date().getFullYear()
</script>

<template>
  <footer>
    <hr />
    <p>Copyright {{ year }} - Mohole</p>
  </footer>
</template>

<style lang="scss" module>
footer {
  p {
    text-align: center;
    font-size: 0.8rem;
    color: #999;
  }
}
</style>