<template>
  <main class="main">
    <FirstPage />
  </main>
</template>

<script>
import FirstPage from "./FirstPage.vue"
/*
import PageHeader from "./PageHeader.vue"
import ThirdPage from "./ThirdPage.vue"
import StaticFooter from "./StaticFooter.vue"
import SecondPage from "./SecondPage.vue"
*/

export default {
  name: "MainPage",
  components: {
    FirstPage,
    /*
    PageHeader,
    SecondPage,
    ThirdPage,
    StaticFooter,
    */
  }
}
</script>

<style scoped>
</style>
