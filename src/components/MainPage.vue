<template>
  <main class="main">
    <PageHeader />
    <PageBody />
    <SecondPage />
    <ThirdPage />
    <StaticFooter />
  </main>
</template>

<script>
import PageHeader from "./PageHeader.vue"
import PageBody from "./PageBody.vue"
import ThirdPage from "./ThirdPage.vue"
import StaticFooter from "./StaticFooter.vue"
import SecondPage from "./SecondPage.vue"

export default {
  name: "MainPage",
  components: {
    PageHeader,
    SecondPage,
    PageBody,
    ThirdPage,
    StaticFooter,
  }
}
</script>

<style scoped>
</style>
