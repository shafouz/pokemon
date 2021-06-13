<template>
  <section>
    <aside>
      <p>Faça seu teste</p>
      <strong>De frontend</strong>
      <p>
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dapibus tortor metus, nec eleifend urna blandit ac. </p>
      <ActionButton />
    </aside>
    <footer class="buttons">
      <div class="arrow-wrapper">
        <RoundedButton image="arrow-left.svg" />
      </div>
      <div class="arrow-wrapper">
        <RoundedButton image="arrow-right.svg" />
      </div>
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
  background-image: url("../assets/hero-banner__image.png");
  background-size: 80%;
  background-position: 250% 60%;
  background-repeat: no-repeat;
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

/* arrow buttons */
.arrow-wrapper {
  margin: 1rem 0.5rem;
}
</style>

