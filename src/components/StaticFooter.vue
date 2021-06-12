<template>
  <section class="static-footer">
    <header>
      &#128231; 
      <strong class="email">email@testeweb.com</strong>
    </header>
    <aside class="social-media">
      <RoundedPill image="facebook.svg" />
      <RoundedPill image="instagram.svg" />
      <RoundedPill image="youtube.svg" />
    </aside>
    <hr>
    <footer>
      <img class="teste" src="../assets/Teste web.svg">
      <p>2020 &#169; Todos os direitos reservados.</p>
      <p>Desenvolvido por</p>
      <img class="logo" src="../assets/logo-yooh.svg">
    </footer>
  </section>
</template>

<script>
import RoundedPill from "./RoundedPill.vue"

export default {
  name: "StaticFooter",
  components: {
    RoundedPill
  }
}
</script>

<style scoped>
.static-footer {
  padding: 2rem 2rem 0 2rem;
  display: flex;
  flex-flow: column;
  align-items: center;
}

.social-media {
  display: flex;
  margin-bottom: 1rem;
}

.rounded-pill {
  margin: 0.5rem 0.5rem;
}

hr {
  color: #666666;
  width: 75vw;
  opacity: 20%;
  margin: 0;
}

header {
  color: #666666;
  margin: 1rem;
}

footer {
  margin: 2rem 0;
  color: #666666;
  display: flex;
  flex-flow: column;
  align-items: center;
}

.teste {
  height: 1.25rem;
}

.logo {
  height: 1.25rem;
  width: 2.5rem;
}

.email {
  margin-left: 0.25rem;
}
</style>
