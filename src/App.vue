<template>
  <div id="app">
    <Mobile />
  </div>
</template>

<script>
import Mobile from './components/Mobile.vue'

export default {
  name: 'App',
  components: {
    Mobile
  }
}
</script>

<style>
/* color palette */
:root {
  --primary-orange: #ff6b18;
  --secondary-orange: #ffebe0;
}

body {
  color: #ff6b18;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 0.8rem;
}
</style>
