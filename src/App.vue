<template>
  <div id="app">
    <MainPage />
  </div>
</template>

<script>
import MainPage from './components/MainPage.vue'

export default {
  name: 'App',
  components: {
    MainPage
  }
}
</script>

<style>
/* color palette */
:root {
  --primary-orange: #ff6b18;
  --secondary-orange: #ffebe0;
  --yellow-orange: #f3be00;
}

body {
  margin: 0;
  color: #ff6b18;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 0.8rem;
}
</style>
