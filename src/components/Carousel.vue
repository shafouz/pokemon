<template>
  <div class="carousel">
    <PokemonCard />
    <RoundedButton class="arrow-left" image="arrow-left.svg" />
    <RoundedButton class="arrow-right" image="arrow-right.svg" />
  </div>
</template>

<script>
import PokemonCard from "./PokemonCard.vue"
import RoundedButton from "./RoundedButton.vue"

export default {
  name: "CardsCarousel",
  components: {
    PokemonCard,
    RoundedButton
  }
}
</script>

<style scoped>
.carousel {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: repeat(3, 1fr);
  grid-auto-flow: row;
}

.pokemon-card {
  grid-area: 1 / 1 / 3 / 5;
  margin-top: 1rem;
  height: 20rem;
  width: 20rem;
}

.arrow-left {
  grid-area: 2 / 1 / 2 / 1;
}

.arrow-right {
  grid-area: 2 / 4 / 2 / 4;
}
</style>
