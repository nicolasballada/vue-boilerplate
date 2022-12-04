<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import LogoSVG from "./assets/logo.svg?component";
</script>

<template>
  <div class='container-fluid'>
    <div class='row'>
      <nav>
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
          <RouterLink to="/reference">Reference</RouterLink>
      </nav>
    </div>
    <div class='row'>
      <div class='wrapper'>
        <RouterView />
      </div>
    </div>
    <div class='row'>
      <div class='footer'>
        <div class='footer-message'>
          <HelloWorld msg="You did it!" />
        </div>
        <div class='footer-img'>
          <LogoSVG alt="Vite logo" class="logo" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.footer {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 3vh;
  margin-bottom: 2vh;
}

.footer-message {
  margin-top: 3vh;
  width: 100%;
  margin-bottom: 2vh;
}

.footer-img {
  max-height: 50vh;
  width: 100px;
}

.wrapper {
    margin: 2vh;
  }

nav {
  display: block;
  font-size: 1rem;
  text-align: center;
  margin-top: 2vh;
  margin-bottom: 2vh;
  max-height: 1vh;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  .footer {
    margin: 1vh;
    padding-left: 5vw;
    padding-right: 5vw;
    justify-content: space-between;
    width: 100%;
  }

  .footer-message {
    margin: 1vh;
    padding: 1vh;
    width: auto;
  }

  .footer-img {
    margin: 1vh;
    padding: 1vh;
    width: 100px;
  }

  .wrapper {
    margin: 2vh;
    padding: 3vh;
    min-height: 60vh;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1.2rem;
    margin: 1vh 1vw;
    padding: 1vh 1vw;
  }
}
</style>
