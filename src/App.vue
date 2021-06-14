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
  --secondary-yellow-orange: #ffd029;
  --primary-gray: #72808E;
  --secondary-gray: #E5E5E5;
  --primary-blue: #00A8D2;
}

body {
  margin: 0;
  color: #ff6b18;
  font-family: Arial, Helvetica, sans-serif;
}
</style>
