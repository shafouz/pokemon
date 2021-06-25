<template>
  <section class="first-page-panel" :style="{ backgroundColor: color }">
    <span class="title">Faça seu teste</span>
    <strong class="subtitle">{{ text }}</strong>
    <p class="text">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dapibus tortor metus, nec eleifend urna blandit ac. </p>
    <ActionButton />
    <div class="bg-wrapper">
    </div>
  </section>
</template>

<script>
import ActionButton from "./ActionButton.vue"

export default {
  props: {
    text: {
      default: "De frontend",
      type: String,
    },
    color: {
      type: String
    }
  },
  name: "FirstPagePanel",
  components: {
    ActionButton
  }
}
</script>

<style scoped>
section {
  position: relative;
  display: grid;
  grid-template-columns: 1.75rem 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 2.70rem 2rem 1fr 1fr 1fr 1fr 1fr 1fr; 
  grid-template-areas: ". . . . ."
  ". title title . ."
  ". subtitle subtitle subtitle ."
  ". text text . ."
  ". text text . ."
  ". action-button action-button action-button ."
  ". . . . ."
  ". . . . .";
  width: 100%;
  flex-shrink: 0;
  color: white;
  align-items: center;
}

#s2 {
  z-index: 997;
}

.title {
  grid-area: title;
}

.subtitle {
  grid-area: subtitle;
  font-weight: 900;
  font-size: 2rem;
}

.text {
  grid-area: text;
}

.action-button {
  grid-area: action-button;
}

.bg-wrapper {
  position: absolute;
  left: 50%;
  width: 20rem;
  height: 20rem;
  background-image: url("../assets/hero-banner__image.png");
  background-position: 0 0;
  background-size: 100% 100%;
  background-repeat: no-repeat;
}

@media (min-width: 768px) {
  .bg-wrapper {
    left: unset;
    right: 0;
  }
}

@media (min-width: 992px) {
  .bg-wrapper {
    position: absolute;
    z-index: 500;
    width: 30rem;
    height: 30rem;
    top: 15vh;
    left: 50%;
  }

  section {
    display: grid;
    grid-template-columns: 6rem 1fr 1fr 1fr 1fr;
    grid-template-rows: 1fr 2.70rem 2rem 1fr 1fr 1fr 1fr 1fr 1fr; 
    grid-template-areas: ". . . . ."
    ". title . . ."
    ". subtitle . . ."
    ". text . . ."
    ". text . . ."
    ". action-button action-button action-button ."
    ". . . . ."
    ". . . . .";
    width: 100%;
    flex-shrink: 0;
    color: white;
    align-items: center;
    margin-bottom: 15vh;
  }

  strong {
    font-size: 3rem;
  }
}
</style>
