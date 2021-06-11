<template>
  <div class="rounded-button">
    <img :src="require(`@/assets/${filename}`)">
  </div>
</template>

<script>
export default {
  props: ["image"],
  name: "RoundedButton",
  data() {
    return {
      filename: this.image
    }
  }
}
</script>

<style scoped>
.rounded-button {
  display: flex;
  justify-content: center;
  margin: 1rem 0.500rem;
  width: 3rem;
  height: 3rem;
  border-radius: 1.5rem;
  box-shadow: 0 0.313rem 0.625rem -0.500rem black;
  background-color: white;
}

img {
  width: min-content;
}
</style>
