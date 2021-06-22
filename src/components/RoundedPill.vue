<template>
  <button class="rounded-pill">
    <img class="media-image" :src="require(`@/assets/${filename}`)">
  </button>
</template>

<script>
export default {
  props: ["image"],
  name: 'RoundedPill',
  data() {
    return {
      filename: this.image
    }
  }
}
</script>

<style scoped>
.rounded-pill {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 2rem;
  width: 2rem;
  border: 1px solid var(--secondary-orange);
  border-radius: 1.5rem;
}

.rounded-pill:hover {
  cursor: pointer;
}

.media-image {
  height: 0.75rem;
  width: 0.75rem;
}
</style>
