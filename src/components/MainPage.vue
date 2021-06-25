<template>
  <main class="main">
    <PageHeader />
    <div class="page-body">
      <FirstPage />
      <div class="q">
      <SecondPage />
      <ThirdPage />
      </div>
    </div>
    <StaticFooter v-if="false" />
  </main>
</template>

<script>
import PageHeader from "./PageHeader.vue"
import FirstPage from "./FirstPage.vue"
import SecondPage from "./SecondPage.vue"
import ThirdPage from "./ThirdPage.vue"
import StaticFooter from "./StaticFooter.vue"

export default {
  name: "MainPage",
  components: {
    PageHeader,
    FirstPage,
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

@media (min-width: 992px) {
  .page-body {
    display: flex;
    flex-flow: column;
    padding: 0 8rem;
    background-color: #E5E5E5;
  }

  .q {
    display: flex;
    flex-flow: row;
  }
}
</style>
