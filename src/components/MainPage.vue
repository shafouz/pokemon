<template>
  <main class="main">
    <PageHeader />
    <FirstPage />
    <SecondPage />
    <ThirdPage />
    <StaticFooter />
  </main>
</template>

<script>
import FirstPage from "./FirstPage.vue"
import PageHeader from "./PageHeader.vue"
import ThirdPage from "./ThirdPage.vue"
import StaticFooter from "./StaticFooter.vue"
import SecondPage from "./SecondPage.vue"

export default {
  name: "MainPage",
  components: {
       FirstPage,
       PageHeader,
       SecondPage,
       ThirdPage,
       StaticFooter,
  },
}
</script>

<style scoped>
.main {
  display: flex;
  flex-flow: column;
}
</style>
