<template>
  <section class="first-page-panel" :style="{ backgroundColor: color }">
    <span class="title">Faça seu teste</span>
    <strong class="subtitle">De frontend</strong>
    <p class="text">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dapibus tortor metus, nec eleifend urna blandit ac. </p>
    <ActionButton />
  </section>
</template>

<script>
import ActionButton from "./ActionButton.vue"

export default {
  props: [ "color" ],
  name: "FirstPagePanel",
  components: {
    ActionButton
  }
}
</script>

<style scoped>
section {
  display: grid;
  grid-template-columns: 1.5rem 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 2rem 1fr 1fr 1fr 1fr 1fr 1fr 1fr; 
  grid-template-areas: ". . . . ."
  ". title title . ."
  ". subtitle subtitle subtitle ."
  ". text text . ."
  ". text text . ."
  ". action-button action-button action-button ."
  ". . . . ."
  ". . . . .";
  background-image: url("../assets/hero-banner__image.png");
  background-size: 85%;
  background-position: 300% 70%;
  background-repeat: no-repeat;
  width: 100%;
  flex-shrink: 0;
  color: white;
  align-items: center;
}

.title {
  grid-area: title;
}

.subtitle {
  grid-area: subtitle;
  font-size: 2rem;
}

.text {
  grid-area: text;
}

.action-button {
  grid-area: action-button;
}
</style>
