<script setup lang="ts">
import GithubCard from "./GithubCard.vue";
</script>
<template>
  <div class="flex flex-wrap mx-auto items-center justify-center">
    <div class="one bold">
      <h1>My Journey</h1>
      <p>My Journey to becoming a developer</p>
      <GithubCard />
    </div>
    <div class="two bold">
      <h1>My Activity</h1>
      <p>My most recent Github Activity</p>
    <GithubCard />
    </div>
  </div>
</template>

<style>
@media only screen and (min-width: 720px) {
  .one,
  .two {
    width: 45%;
    margin: 3px;
  }
}
</style>
