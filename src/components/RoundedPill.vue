<template>
  <div class="rounded-pill">
    <img class="media-image" :src="require(`@/assets/${filename}`)">
  </div>
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
  height: 2.5rem;
  width: 2.5rem;
  border: 1px solid var(--secondary-orange);
  border-radius: 1.25rem;
}

.media-image {
  height: 1.5rem;
  width: 1.5rem;
}
</style>
