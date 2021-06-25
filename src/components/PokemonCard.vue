<template>
  <div :style="{width: width, height: height}" class="pokemon-card">
    <strong v-if="name" class="pokemon-name">{{ name }}</strong>
    <div class="card-body">
    <ProfileAvatar />
    <strong class="card-title">{{ name }}</strong>
    </div>
  </div>
</template>

<script>
import ProfileAvatar from "./ProfileAvatar.vue"

export default {
  components: {
    ProfileAvatar
  },
  props: {
    name: {
      type: String
    },
    height: {
      type: String,
    },
    width: {
      type: String,
    }
  },
}
</script>

<style scoped>
.card-body {
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas: ". . favorite-icon"
        ". profile-avatar . "
        ". name .";
  place-items: center;
  width: 100%;
  min-height: 12rem;
  height: 100%;
  box-shadow: 0px 4px 4px 0px #0000000D;
  border-radius: 6px;
  background-color: #FBFBFB;
}

.card-title {
  grid-area: name;
  margin-bottom: 2rem;
}

.profile-avatar {
  grid-area: profile-avatar;
}

.pokemon-name {
  align-self: start;
  color: var(--primary-gray);
  font-size: 1.5rem;
  line-height: 1.75rem;
}

@media (min-width: 992px) {
  .pokemon-card {
    height: 100%;
    width: 100%;
  }

  .card-body {
    margin-top: 1rem;
  }
}
</style>
