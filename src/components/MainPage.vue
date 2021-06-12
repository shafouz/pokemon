<template>
  <main class="main">
    <SecondPage />
  </main>
</template>

<script>
/*
import PageBody from "./PageBody.vue"
import ThirdPage from "./ThirdPage.vue"
import StaticFooter from "./StaticFooter.vue"
*/
import SecondPage from "./SecondPage.vue"

export default {
  name: "MainPage",
  components: {
    SecondPage,
    /*
    PageBody,
    ThirdPage,
    StaticFooter,
    */
  }
}
</script>

<style scoped>
</style>
