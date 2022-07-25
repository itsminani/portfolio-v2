<script setup lang="ts">
import { reactive,ref } from "vue";
const result = ref(null)
// Implementation code where T is the returned data shape

function fetchData(){
    fetch("https://api.github.com/users/itsminani/events/public")
        .then(response =>response.json())
        .then(data => result.value = data)
        .then(data => console.log(data))
    return result.value
}


console.log(fetchData())

const card = reactive({
  title: "Noteworthy technology acquisitions 2021",
  description:
    "Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.",
  image: "https://www.kindpng.com/picc/m/42-427622_cat-png-transparent-png.png",
  image2: "src/assets/Parallax/anime_girl.png",
  img_alt: "Project Image",
});
</script>

<template>
  <ol class="relative m-5 border-l border-gray-200 dark:border-gray-700">
    <li class="mb-10 ml-6">
      <span
        class="flex absolute -left-3 justify-center items-center w-6 h-6 bg-blue-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-blue-900"
      >
        <img
          class="rounded-full shadow-lg"
          src="src/assets/Parallax/anime_girl.png"
          alt="Bonnie image"
        />
      </span>
      <div
        class="justify-between items-center p-4 rounded-lg border border-gray-200 shadow-sm sm:flex dark:border-gray-600"
      >
        <time
          class="mb-1 text-xs font-normal text-gray-400 sm:order-last sm:mb-0"
          >just now</time
        >
        <div class="text-sm font-normal">
          Bonnie moved
          <a
            href="#"
            class="font-semibold text-blue-600 dark:text-blue-500 hover:underline"
            >Jese Leos</a
          >
          to
          <span
            class="bg-gray-100 text-gray-800 text-xs font-normal mr-2 px-2.5 py-0.5 rounded dark:bg-gray-600 dark:text-gray-300"
            >Funny Group</span
          >
        </div>
      </div>
    </li>
    <li class="mb-10 ml-6">
      <span
        class="flex absolute -left-3 justify-center items-center w-6 h-6 rounded-full ring-8 ring-white dark:ring-gray-900"
      >
        <img
          class="rounded-full shadow-lg"
          src="src/assets/Parallax/anime_girl.png"
          alt="Thomas Lean image"
        />
      </span>
      <div
        class="p-4 primary rounded-lg border border-gray-200 shadow-sm dark:border-gray-600"
      >
        <div class="justify-between items-center mb-3 sm:flex">
          <time
            class="mb-1 text-xs font-normal text-gray-400 sm:order-last sm:mb-0"
            >2 hours ago</time
          >
          <div class="text-sm font-normal lex">
            Thomas Lean commented on
            <a
              href="#"
              class="font-semibold text-blue-600 dark:text-blue-500 hover:underline"
              >Flowbite Pro</a
            >
          </div>
        </div>
        <div
          class="p-3 text-xs italic font-normal text-gray-500 bg-gray-50 rounded-lg border border-gray-200 dark:bg-gray-600 dark:border-gray-500 dark:text-gray-300"
        >
          Hi ya'll! I wanted to share a webinar zeroheight is having regarding
          how to best measure your design system! This is the second session of
          our new webinar series on #DesignSystems discussions where we'll be
          speaking about Measurement.
        </div>
      </div>
    </li>
    <li class="ml-6">
      <span
        class="flex absolute -left-3 justify-center items-center w-6 h-6 bg-blue-200 rounded-full ring-8 ring-white dark:ring-gray-900 dark:bg-blue-900"
      >
        <img
          class="rounded-full shadow-lg"
          src="src/assets/Parallax/anime_girl.png"
          alt="Jese Leos image"
        />
      </span>
      <div
        class="justify-between items-center p-4 rounded-lg border border-gray-200 shadow-sm sm:flex dark:border-gray-600"
      >
        <time
          class="mb-1 text-xs font-normal text-gray-400 sm:order-last sm:mb-0"
          >1 day ago</time
        >
        <div class="text-sm font-normal lex">
          Jese Leos has changed
          <a
            href="#"
            class="font-semibold text-blue-600 dark:text-blue-500 hover:underline"
            >Pricing page</a
          >
          task status to
          <span class="font-semibold">Finished</span>
        </div>
      </div>
    </li>
  </ol>
</template>

<style>
.projectCard {
  background-color: var(--highlight-color);
}

img {
}
</style>
