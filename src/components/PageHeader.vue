<template>
  <header>
    <img class="menu" src="../assets/menu.svg">
    <div class="teste-wrapper">
      <img src="../assets/Teste web.svg">
    </div>
    <ActionButton text="Login at GitHub" />
    <div class="pills-wrapper">
      <RoundedPill image="facebook.svg" />
      <RoundedPill image="instagram.svg" />
      <RoundedPill image="youtube.svg" />
    </div>
  </header>
</template>

<script>
import RoundedPill from "./RoundedPill.vue"
import ActionButton from "./ActionButton.vue"

export default {
  name: "PageHeader",
  components: {
    RoundedPill,
    ActionButton
  }
}
</script>

<style scoped>
img:hover {
  cursor: pointer;
}

header {
  display: grid;
  grid-template-columns: [nav] 1rem [title] 4fr [pills] 1fr;
  align-items: center;
  grid-column-gap: 0.325rem;
  padding: 0 1rem;
  height: 5rem;
}

.teste-wrapper {
  display: flex;
  align-self: center;
  margin-left: 2rem;
}

.teste-wrapper img {
  height: 1.2rem;
}

.rounded-pill {
  margin-right: 0.625rem;
}

.pills-wrapper {
  display: flex;
  justify-content: flex-end;
}

.action-button {
  display: none;
}

@media (min-width: 992px) {
  header {
    display: grid;
    grid-template-columns: [nav] 1rem [title] 3fr [github] 1fr [pills] 1fr;
    align-items: center;
    grid-column-gap: 0.325rem;
    padding: 0 9.75rem;
    height: 5rem;
  }

  .action-button {
    display: block;
    margin: 0;
  }
}
</style>
