<template>
  <main class="main">
    <PageHeader />
    <PageBody />
  </main>
</template>

<script>
import PageHeader from "./PageHeader.vue"
import PageBody from "./PageBody.vue"

export default {
  name: "MainPage",
  components: {
    PageHeader,
    PageBody
  }
}
</script>

<style scoped>
</style>
