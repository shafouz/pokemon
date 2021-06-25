<template>
  <section class="secondary-page">
    <strong>Últimos pokemons</strong>
    <section class="cards">
      <PokemonCard width="15%" v-for="item in 6" :key="item" />
    </section>
    <section class="cards-carousel">
      <SecondPageCarousel />
    </section>
  </section>
</template>

<script>
import SecondPageCarousel from "./SecondPageCarousel.vue"
import PokemonCard from "./PokemonCard.vue"

export default {
  name: "SecondPage",
  components: {
    SecondPageCarousel,
    PokemonCard,
  }
}
</script>

<style scoped>
/* first section */
.secondary-page {
  padding: 1.5rem 2.25rem 0 2.25rem;
  background-color: var(--secondary-gray);
}

.cards {
  display: flex;
  flex-flow: row;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: 1rem 0 3rem 0; 
}

.pokemon-card {
  margin-bottom: 0.5rem;
}

/* both sections */
strong {
  color: var(--primary-gray);
  font-size: 1.5rem;
  line-height: 1.75rem;
}

@media (min-width: 992px) {
  .secondary-page {
    padding: unset;
  }

  .cards-carousel {
    width: 50%;
  }

  .card-wrapper {
    width: 15%;
  }
}
</style>
