<template>
  <div class="first-page-wrapper">
    <transition name="slide" mode="in-out">
    <section v-if="change" key="orange">
      <aside>
        <p>Faça seu teste</p>
        <strong>De frontend</strong>
        <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dapibus tortor metus, nec eleifend urna blandit ac. </p>
        <ActionButton />
      </aside>
      <footer class="buttons">
        <div @click="changeSlide('left')" class="arrow-wrapper">
          <RoundedButton  image="arrow-left.svg" />
        </div>
        <div @click="changeSlide('right')" class="arrow-wrapper">
          <RoundedButton image="arrow-right.svg" />
        </div>
      </footer>
    </section>
    <section style="backgroundColor: blue" key="blue" v-else>
      <aside>
        <p>Faça seu teste</p>
        <strong>De frontend</strong>
        <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce dapibus tortor metus, nec eleifend urna blandit ac. </p>
        <ActionButton />
      </aside>
      <footer class="buttons">
        <div @click="changeSlide('left')" class="arrow-wrapper">
          <RoundedButton  image="arrow-left.svg" />
        </div>
        <div @click="changeSlide('right')" class="arrow-wrapper">
          <RoundedButton image="arrow-right.svg" />
        </div>
      </footer>
    </section>
    </transition>
  </div>
</template>

<script>
import RoundedButton from "./RoundedButton.vue"
import ActionButton from "./ActionButton.vue"

export default {
  name: "PageBody",
  components: {
    RoundedButton,
    ActionButton
  },
  data() {
    return {
      change: true
    }
  },
  methods: {
    changeSlide(direction) {
      this.change = !this.change
      console.log(direction)
    }
  }
}
</script>

<style scoped>
/* body */
.first-page-wrapper {
  display: flex;
  flex-flow: row;
}

section {
  position: absolute;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 2fr 1fr 1fr 1fr; 
  background-image: url("../assets/hero-banner__image.png");
  background-color: var(--yellow-orange);
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

/* transition */
.slide-enter-active {
  transition: all 2s;
}

.slide-leave-active {
  transition: all 2s;
  transform: translateX(100%);
}

.slide-enter, .slide-leave {
  transform: translateX(100%);
}
/*
.slide-b-enter-active {
transition: all .3s;
}

.slide-b-leave-active {
transition: all;
transition-delay: .3s;
}

.slide-b-enter, .slide-b-leave-to
{
transform: translateX(-1000px);
}
 */
</style>

