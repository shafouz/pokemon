<template>
  <div class="first-page-wrapper">
    <div class="carousel">
      <FirstPagePanel id="s1" color="#f3be00" />
      <FirstPagePanel id="s2" color="#00A8D2" />
      <footer class="buttons">
        <div @click="prev" class="arrow-wrapper">
          <RoundedButton image="arrow-left.svg" />
        </div>
        <div @click="next" class="arrow-wrapper">
          <RoundedButton image="arrow-right.svg" />
        </div>
      </footer>
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
      if (this.currentIndex == 1) { document.getElementById("s1").scrollIntoView({behavior: "smooth"}) }
      if (this.currentIndex == 2) { document.getElementById("s2").scrollIntoView({behavior: "smooth"}) }
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

/* arrow buttons */
.buttons {
  flex: none;
  display: flex;
  justify-content: center;
  position: absolute;
  align-self: end;
  left: 0;
  right: 0;
  margin: 0 auto;
}

.arrow-wrapper {
  margin: 1rem 0.5rem;
}
</style>

