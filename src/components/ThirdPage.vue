<template>
  <section class="third-page">
    <strong> Test frontend</strong>
    <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nisi, a lacus, aliquam mattis est enim, molestie diam. Consequat blandit nec, venenatis dignissim suspendisse in facilisi molestie duis. Tempor sed quis phasellus arcu, posuere. Elementum ut tellus nisi, nunc ac etiam ut lectus porta. Et morbi enim vestibulum sodales sed ullamcorper dapibus accumsan. Faucibus pharetra, et at orci, vel blandit odio. Volutpat urna fusce quisque libero pellentesque in. Augue tempor vitae ullamcorper bibendum.

Quis facilisi nulla id est natoque sed ut consectetur. Id eleifend eros ullamcorper et. Diam, ultrices pellentesque urna, integer a lectus. Sit sollicitudin ac egestas amet netus. Elit vitae dolor cursus cursus.
    </p>
    <ActionButton />
  </section>
</template>

<script>
import ActionButton from "./ActionButton.vue"

export default {
  name: "ThirdPage",
  components: {
    ActionButton
  }

}
</script>

<style scoped>
.third-page {
  background-color: var(--secondary-yellow-orange);
  padding: 2.5rem;
  display: flex;
  justify-content: center;
  flex-flow: column;
}

strong {
  font-size: 1.5rem;
}

p {
  color: black;
  line-height: 1.25rem;
  padding: 1rem 0;
}

.action-button {
  margin: auto;
}

@media (min-width: 992px) {
  .third-page {
    height: 100%;
    width: 50%;
  }
}
</style>

