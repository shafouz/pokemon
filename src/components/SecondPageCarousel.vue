<template>
  <div class="carousel">
    <strong class="pokemon-name">Pokemon Name</strong>
    <div class="cards-wrapper">
      <PokemonCard v-for="item in 4" :key="item" class="card" :id="`card-${item}`" />
    </div>
    <div @click="prev" class="arrow-wrapper">
      <RoundedButton class="arrow-left" image="arrow-left.svg" />
    </div>
    <div @click="next" class="arrow-wrapper">
      <RoundedButton class="arrow-right" image="arrow-right.svg" />
    </div>
    <div class="carousel-pills">
      <div v-for="item in 4" :key="item" class="pill" :id="`pill-${item}`">
      </div>
    </div>
  </div>
</template>

<script>
import PokemonCard from "./PokemonCard.vue"
import RoundedButton from "./RoundedButton.vue"

export default {
  name: "SecondPageCarousel",
  components: {
    PokemonCard,
    RoundedButton
  },
  data() {
    return {
      currentIndex: 1,
    }
  },
  methods: {
    next() {
      if ( this.currentIndex == 4 ) { return this.currentIndex = 1 }
      this.currentIndex += 1;
    },
    prev() {
      if ( this.currentIndex == 1 ) { return this.currentIndex = 4 }
      this.currentIndex -= 1;
    },
  },
  watch: {
    currentIndex() {
      // cards
      document.getElementById(`card-${this.currentIndex}`).scrollIntoView({
        behavior: 'smooth',
        block: 'nearest',
        inline: 'start'
      })

      //pills
      for (let i = 1; i <= 4; i++) {
        document.getElementById(`pill-${i}`).classList.remove("active")
      }

      document.getElementById(`pill-${this.currentIndex}`).classList.toggle("active")
    }
  },
  mounted() {
    this.currentIndex = 1
    document.getElementById(`pill-1`).classList.toggle("active")
  }
}
</script>

<style scoped>
.carousel {
  position: relative;
  display: flex;
  flex-flow: column;
}

.cards-wrapper {
  flex: none;
  width: 100%;
  height: 70vw;
  display: flex;
  flex-flow: row;
  align-items: center;
  overflow-x: hidden;
  padding: 4px 0;
  border-radius: 6px;
}

.card {
  margin: 0 0.5rem;
}

.pokemon-name {
  margin: 1rem 0 1rem 0.5rem;
  align-self: start;
  color: var(--primary-gray);
  font-size: 1.5rem;
  line-height: 1.75rem;
}

.pokemon-card {
  flex-shrink: 0;
  width: 100%;
  height: 100%;
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.05);
}

.arrow-left {
  position: absolute;
  margin-left: -1.5rem;
  bottom: calc(50%);
}

.arrow-right {
  position: absolute;
  right: 0;
  margin-right: -1.5rem;
  bottom: calc(50%);
}

.carousel-pills {
  margin: 1.5rem 0 3.25rem 0;
  align-self: center;
  display: flex;
}

.pill {
  width: 0.75rem;
  height: 0.75rem;
  background-color: #C4C4C4;
  border-radius: 0.375rem;
  margin: 0.5rem;
}

.pill.active {
  background-color: var(--primary-orange);
}
</style>
