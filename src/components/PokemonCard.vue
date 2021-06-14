<template>
  <div class="pokemon-card">
    <ProfileAvatar />
    <strong>Nome</strong>
  </div>
</template>

<script>
import ProfileAvatar from "./ProfileAvatar.vue"

export default {
  components: {
    ProfileAvatar
  }
}
</script>

<style scoped>
.pokemon-card {
  display: grid;
  grid: ". . favorite-icon"
        ". profile-avatar . "
        ". name .";
  place-items: center;
  width: 48.5%;
  height: 11.25rem;
  box-shadow: 0px 4px 4px 0px #0000000D;
  border-radius: 6px;
  background-color: #FBFBFB;
}

strong {
  grid-area: name;
  margin-bottom: 2rem;
}

.profile-avatar {
  grid-area: profile-avatar;
}
</style>
