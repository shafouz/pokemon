<template>
  <button class="rounded-button">
    <img :src="require(`@/assets/${filename}`)">
  </button>
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
  width: 3rem;
  height: 3rem;
  border: none;
  border-radius: 1.5rem;
  box-shadow: 0px 4px 4px 0px #0000001A;
  background-color: white;
}

.rounded-button:hover {
  cursor: pointer;
  background-color: whitesmoke;
}

img {
  width: min-content;
}
</style>
