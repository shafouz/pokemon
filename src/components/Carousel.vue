<template>
  <div class="carousel">
    <PokemonCard />
    <RoundedButton class="arrow-left" image="arrow-left.svg" />
    <RoundedButton class="arrow-right" image="arrow-right.svg" />
    <div class="carousel-pills">
      <div v-for="item in 4" :key="item" class="pill">
      </div>
    </div>
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
  grid-template-rows: repeat(4, 1fr);
  grid-auto-flow: row;
  align-items: center;
  margin: 0 0 1.25rem 0;
}

.pokemon-card {
  grid-area: 1 / 2 / 4 / 5;
  width: 19.25rem;
  height: 16rem;
  justify-self: center;
}

.arrow-left {
  grid-area: 2 / 1;
  justify-self: start;
  margin-left: -1.5rem;
}

.arrow-right {
  grid-area: 2 / 5;
  justify-self: end;
  margin-right: -1.5rem;
}

.carousel-pills {
  grid-area: 4 / 3;
  display: flex;
  justify-content: center;
}

.pill {
  width: 0.75rem;
  height: 0.75rem;
  background-color: #C4C4C4;
  border-radius: 0.375rem;
  margin: 0.5rem;
}
</style>
