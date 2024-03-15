<script setup>
  import Header from './components/Header-item.vue'
  import Main from './components/Main-item.vue'
  import Footer from './components/Footer-item.vue'
</script>

<template>
  <!-- connect fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <!-- Michroma.Monserrat -->
    <link href="https://fonts.googleapis.com/css2?family=Michroma&family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
  <!-- connect fonts -->
  <div>
    <Header></Header>
    <Main></Main>
    <Footer></Footer>
  </div>
</template>

<style scoped>
</style>
