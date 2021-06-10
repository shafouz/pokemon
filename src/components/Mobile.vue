<template>
  <header>
    <nav>
      <img src="../assets/menu.svg">
    </nav>
    <h1>
      Test web
    </h1>
    <ul>
    <RoundedPill image="instagram.svg" />
    <RoundedPill image="facebook.svg" />
    <RoundedPill image="youtube.svg" />
    </ul>
  </header>
</template>

<script>
import RoundedPill from "./RoundedPill.vue"

export default {
  components: {
    RoundedPill
  }
}
</script>

<style scoped>
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0;
  padding: 0;
  width: 95vw;
  height: 3.5rem;
  border-bottom: 2px solid black;
}

nav {
	display: flex;
	justify-content: center;
	align-items: center;
  height: 2.5rem;
  width: 2.5rem;
}

ul {
  display: flex;
  justify-content: end;
}
</style>
