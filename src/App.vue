<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from "./components/HelloWorld.vue";
import ToggleDark from "./components/ToggleDark.vue";
import NavBar from "./components/NavBar.vue";
import ParallaxCard from "./components/ParallaxCard.vue";
</script>

<template class="flex items-center justify-center h-screen">
  <div class="app ">
    <NavBar />
    <ParallaxCard />
    <h1>MBOKOLO ASHOBORA KUBA ARENZE NDAQ</h1>
    <div>
      <a href="#" target="">
        <img src="/vite.svg" class="logo" alt="Vite logo" />
      </a>
      <a href="#" target="">
        <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
      </a>
    </div>
    <ToggleDark />
    <HelloWorld msg="Vite + Vue" />
  </div>
</template>

<style scoped>
.app{
  width: 100%;
}
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

<style></style>
