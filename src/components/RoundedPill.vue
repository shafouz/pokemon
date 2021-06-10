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
  height: 1.75rem;
  width: 1.75rem;
  border: 1px solid var(--secondary-orange);
  border-radius: 1.25rem;
}

.media-image {
  height: 0.75rem;
  width: 0.75rem;
}
</style>
