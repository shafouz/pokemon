<template>
  <div class="first-page-wrapper">
    <div class="carousel">
      <FirstPagePanel id="s1" color="#f3be00" />
      <FirstPagePanel id="s2" color="#00A8D2" text="Outro Banner" />
    </div>
    <div @click="prev" class="arrow-wrapper left">
      <RoundedButton image="arrow-left.svg" />
    </div>
    <div @click="next" class="arrow-wrapper right">
      <RoundedButton image="arrow-right.svg" />
    </div>
  </div>
</template>

<script>
import FirstPagePanel from "./FirstPagePanel.vue"
import RoundedButton from "./RoundedButton.vue"

export default {
  name: "PageBody",
  components: {
    FirstPagePanel,
    RoundedButton,
  },
  data() {
    return {
      currentIndex: 1,
    }
  },
  methods: {
    next() {
      if ( this.currentIndex == 2 ) { return this.currentIndex = 1 }
      this.currentIndex += 1;
    },
    prev() {
      if ( this.currentIndex == 1 ) { return this.currentIndex = 2 }
      this.currentIndex -= 1;
    },
  },
  watch: {
    currentIndex() {
      document.getElementById(`s${this.currentIndex}`).scrollIntoView({
        behavior: 'smooth',
        block: 'nearest',
        inline: 'start'
      })
    }
  }
}
</script>

<style scoped>
/* body */
.carousel {
  display: flex;
  flex-flow: row;
  overflow-x: hidden;
}

.arrow-wrapper {
  margin: 1rem 0.5rem;
}

@media (min-width: 992px) {
  .first-page-wrapper {
    margin-top: 2rem;
    position: relative;
  }

  .arrow-wrapper {
    position: absolute;
    margin: unset;
    z-index: 999;
  }

  .left {
    position: absolute;
    z-index: 998;
    left: 0;
    top: 37%;
    margin-left: -1.5rem;
  }

  .right {
    position: absolute;
    z-index: 998;
    right: 0;
    top: 37%;
    margin-right: -1.5rem;
  }
}
</style>

