<template>
  <Header />
  <main class="container">
    <slot />
    <Footer />
  </main>
</template>

<style scoped>
main {
  padding: 1rem 0;
}
</style>