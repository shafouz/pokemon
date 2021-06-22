<template>
  <button class="action-button" href="#"><strong>{{ text }}</strong></button>
</template>

<script>
export default {
  name: "ActionButton",
  props: {
    text: {
      default: "CALL TO ACTION",
      type: String
    }
  }
}
</script>

<style scoped>
button {
  margin-top: 1rem;
  background-color: var(--primary-orange);
  color: white;
  border: none;
  height: 2.75rem;
  width: 45vw;
  max-width: 15rem;
  border-radius: 1.375rem;
}

button:hover {
  cursor: pointer;
  background-color: #ff6b01;
}
</style>
