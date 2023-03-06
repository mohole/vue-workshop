<template>
  <Header />
  <main class="container">
    <slot />
    <Footer />
  </main>
</template>

<style module>
main {
  padding: 1rem 0;
}
</style>