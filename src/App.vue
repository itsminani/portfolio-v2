<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from "./components/HelloWorld.vue";
import ToggleDark from "./components/ToggleDark.vue";
import NavBar from "./components/NavBar.vue";
import ParallaxCard from "./components/ParallaxCard.vue";
import Card from "./components/ProjectCard.vue";
import GithubHero from "./components/GithubHero.vue";
</script>
<template class="">
  <div id="your-element-selector"></div>
  <div class=" ">
    <NavBar id="nav" />
    <div class="container mx-auto px-2">
      <ParallaxCard />
      <GithubHero />
      <div class="flex flex-wrap gap-3">
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
        <Card />
      </div>
      <!-- <h1>MBOKOLO ASHOBORA KUBA ARENZE NDAQ dsfkljdsfj;ksfdjjlsfajlfsdjjfsdkl</h1> -->
      <div class="flex">
        <a href="#" target="">
          <img src="/vite.svg" class="logo" alt="Vite logo" />
        </a>
        <a href="#" target="">
          <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
        </a>
      </div>
      <ToggleDark />
      <HelloWorld msg="Vite + Vue" /> -->
    </div>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}

/* Set the width to 100vw */
#nav {
  width: 100vw;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>

<style></style>
