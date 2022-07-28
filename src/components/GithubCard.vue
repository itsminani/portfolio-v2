<script setup lang="ts">
import { reactive, ref } from "vue";

interface githubApiResults {
   [k: string]: string;
}
const results= ref<HTMLDivElement>();
// "https://api.github.com/users/itsminani/events/public

const getData = fetch("https://api.github.com/users/itsminani/events/public")
  .then((response) => response.json())
  .then((data) => (results.value = data));

const userActivity = async () => {
  const a = await getData;
  console.log(a);
  return a;
};

let bruv = userActivity();
console.log(bruv);
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
  <!-- <p>{{results}}</p> -->
  <div class="scroller mb-5 mt-3 border-y border-gray-200 dark:border-gray-700">
    <ol
      v-if="results"
      class="relative m-5 border-l border-gray-200 dark:border-gray-700"
    >
      <div v-for="result in results" v-bind:key="result?.id">
        <li v-if="result?.type == 'PushEvent'" class="mb-10 ml-6">
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
                itsminani pushed a commit to
                <a
                  href="#"
                  class="font-semibold text-blue-600 dark:text-blue-500 hover:underline"
                >
                  {{ result.repo.name }}
                </a>
                <span
                  class="ml-2 bg-gray-100 text-gray-800 text-xs font-normal mr-2 px-2.5 py-0.5 rounded dark:bg-gray-600 dark:text-gray-300"
                  >{{ result.payload.ref }}</span
                >
              </div>
            </div>
            <div
              v-if="result.payload.commits"
              class="p-3 text-xs italic font-normal text-gray-500 bg-gray-50 rounded-lg border border-gray-200 dark:bg-gray-600 dark:border-gray-500 dark:text-gray-300"
            >
              {{ result.payload.commits[0].message }}
            </div>
          </div>
        </li>
      </div>
    </ol>
  </div>
</template>

<style>
.scroller{
    overflow-y:scroll;
    height: 87vh;
}
.projectCard {
  background-color: var(--highlight-color);
}

img {
}
</style>
