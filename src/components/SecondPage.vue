<template>
  <section class="secondary-page">
    <section class="cards">
      <strong>Últimos pokemons</strong>
      <PokemonCard v-for="item in 8" :key="item" />
    </section>
    <section class="cards-carousel">
      <strong class="pokemon-name">Pokemon Name</strong>
      <Carousel />
    </section>
  </section>
</template>

<script>
import Carousel from "./Carousel.vue"
import PokemonCard from "./PokemonCard.vue"

export default {
  name: "SecondPage",
  components: {
    Carousel,
    PokemonCard,
  }
}
</script>

<style scoped>
.secondary-page {
  padding: 0rem 2.25rem;
  background-color: var(--secondary-gray);
}

.cards {
  display: flex;
  flex-flow: row;
  flex-wrap: wrap;
  margin-bottom: 4rem;
}

strong {
  color: var(--primary-gray);
  font-size: 1.5rem;
  line-height: 1.75rem;
  margin-bottom: 1rem;
  margin-top: 2rem;
}

.pokemon-card {
  flex-shrink: 0;
}

.pokemon-card:nth-child(even) {
  margin-right: 0.75rem;
  margin-bottom: 0.75rem;
}
</style>

