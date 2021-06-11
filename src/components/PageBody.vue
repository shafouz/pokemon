<template>
  <section>
    <aside>
      <h1>Faça seu teste</h1>
      <strong>De frontend</strong>
      <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dapibus tortor metus, nec eleifend urna blandit ac. </p>
      <ActionButton />
    </aside>
    <footer class="buttons">
      <RoundedButton image="arrow-left.svg" />
      <RoundedButton image="arrow-right.svg" />
    </footer>
  </section>
</template>

<script>
import RoundedButton from "./RoundedButton.vue"
import ActionButton from "./ActionButton.vue"

export default {
  name: "PageBody",
  components: {
    RoundedButton,
    ActionButton
  }
}
</script>

<style scoped>
/* body */
section {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 2fr 1fr 1fr 1fr; 
  background-color: var(--yellow-orange);
}

/* aside */
aside {
  display: flex;
  flex-flow: column;
  margin-left: 1.5rem;
  grid-area: 2 / 1 / 4 / 3;
  color: white;
}

strong {
  font-size: 1.33rem;
}

/* footer */
footer {
  display: flex;
  grid-area: 5 / 2 / 5 / 4;
  place-self: end center;
}
</style>

