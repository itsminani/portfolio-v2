<script setup lang="ts">
import {reactive} from "vue"
const card = reactive({
    title: "Noteworthy technology acquisitions 2021",
    description: "Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.",
    image: "https://www.kindpng.com/picc/m/42-427622_cat-png-transparent-png.png",
    image2: "src/assets/Parallax/anime_girl.png",
    img_alt: "Project Image",

})
</script>

<template>
<div class="projectCard m-auto max-w-sm  rounded-lg border border-gray-200 shadow-md">
    <a href="#">
        <img class="rounded-t-lg" :src="card.image2" :alt="card.image2+card.img_alt"/>
    </a>
    <div class="p-5">
        <a href="#">
            <h5 class="mb-2 text-2xl font-bold tracking-tight ">{{card.title}}</h5>
        </a>
        <p class="mb-3 font-normal">{{card.description}}</p>
        <a href="#" class="inline-flex items-center py-2 px-3 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
            Read more
            <svg aria-hidden="true" class="ml-2 -mr-1 w-4 h-4" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
        </a>
    </div>
</div>
  
</template>

<style>
.projectCard{
  background-color: var(--highlight-color);
}

img{
}
</style>