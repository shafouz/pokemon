<template>
  <header>
    <img src="../assets/menu.svg">
    <h1>
      Teste web
    </h1>
    <RoundedPill image="facebook.svg" />
    <RoundedPill image="instagram.svg" />
    <RoundedPill image="youtube.svg" />
  </header>
</template>

<script>
import RoundedPill from "./RoundedPill.vue"

export default {
  name: "PageHeader",
  components: {
    RoundedPill
  }
}
</script>

<style scoped>
header {
  display: grid;
  grid-template-columns: [nav] 1fr [title] 4fr [pill1] 1fr [pill2] 1fr [pill3] 1fr;
  align-items: center;
  grid-column-gap: 0.325rem;

  padding: 0 1rem;
}

nav {
  height: 2.5rem;
  width: 2.5rem;
  align-self: center;
  justify-self: center;
}
</style>
