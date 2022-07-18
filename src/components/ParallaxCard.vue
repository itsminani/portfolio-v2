<script setup lang="ts">
import { computed, reactive, ref } from "vue";
import type { CSSProperties } from "vue";
import { autoResetRef, useMediaQuery, useParallax } from "@vueuse/core";
const target = ref(null);

const showLayer0 = ref(true)  
const showLayer1 = ref(true)  
const showLayer2 = ref(true)  
const showLayer3 = ref(true)  
const showLayer4 = ref(true)  

const isMobile = useMediaQuery("(max-width: 700px)");
const parallax = reactive(useParallax(target));
const targetStyle: CSSProperties = {
  display: "flex",
  flexDirection: "column",
  justifyContent: "center",
  minHeight: "500px",
  transition: ".3s ease-out all",
};
const cardWindowStyle: CSSProperties = {
  overflow: "hidden",
  fontSize: "6rem",
  position: "absolute",
  top: "calc(50% - 2em)",
  left: "calc(50% - 2em)",
  height: "4em",
  width: "4em",
  margin: "auto",
};
const layerBase: CSSProperties = {
  position: "absolute",
  height: "100%",
  width: "100%",
  transition: ".3s ease-out all",
};
const containerStyle: CSSProperties = {
  margin: "3em auto",
  perspective: "500px",
};
const infoStyle = computed(() => ({
  opacity: 0.4,
  top: "20px",
  left: "40px",
  position: isMobile.value ? "inherit" : "absolute",
}));
const layer0 = computed(() => ({
  ...layerBase,
  transform: `translateX(${parallax.tilt * 10}px) translateY(${
    parallax.roll * 10
  }px) scale(1.33)`,
}));
const layer1 = computed(() => ({
  ...layerBase,
  transform: `translateX(${parallax.tilt * 20}px) translateY(${
    parallax.roll * 20
  }px) scale(1.33)`,
}));
const layer2 = computed(() => ({
  ...layerBase,
  transform: `translateX(${parallax.tilt * 30}px) translateY(${
    parallax.roll * 30
  }px) scale(1.33)`,
}));
const layer3 = computed(() => ({
  ...layerBase,
  transform: `translateX(${parallax.tilt * 40}px) translateY(${
    parallax.roll * 40
  }px) scale(0.90)`,
}));
const layer4 = layerBase;
const cardStyle = computed(() => ({
  background: "#fff",
  borderRadius: "5px",
  border: "1px solid #cdcdcd",
  overflow: "hidden",
  transition: ".3s ease-out all",
  boxShadow: "0 0 20px 0 rgba(255, 255, 255, 0.25)",
  transform: `rotateX(${parallax.roll * 20}deg) rotateY(${
    parallax.tilt * 20
  }deg)`,
}));
</script>

<!-- Parallax effect using Vueuse Module
    Inspiration comes from how this was used on Vueuse's website
 -->

<template>
  <div>
    <div ref="target" :style="targetStyle">
      <div :style="containerStyle">
        <div class="card" :style="cardStyle">
          <div :style="cardWindowStyle">
          <Transition >
              <img
                :style="layer0"
                v-if="showLayer0"
                src="../assets/Parallax/page2layer0_new.png"
                alt=""
              />
          
          </Transition>
            <img
              :style="layer1"
              v-if="showLayer1"
              src="../assets/Parallax/page2layer1_new.png"
              alt=""
            />
            <img
              :style="layer2"
              v-if="showLayer2"
              src="../assets/Parallax/page2layer2_new.png"
              alt=""
            />
            <img
              :style="layer3"
              v-if="showLayer3"
              src="../assets/Parallax/page2layer3_new.png"
              alt=""
            />
            <img
              :style="layer4"
              v-if="showLayer4"
              src="../assets/Parallax/page2layer4_new.png"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>

    <div>
      <label
        for="default-toggle"
        class="inline-flex relative items-center cursor-pointer"
      >
        <input
          type="checkbox"
          v-model="showLayer1"
          id="default-toggle"
          class="sr-only peer"
        />
        <div
          class="w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-blue-600"
        ></div>
        <span class="ml-3 text-sm font-medium">Front-end Technologies?</span>
      </label>
      <label
        for="default-toggle2"
        class="inline-flex relative items-center cursor-pointer"
      >
        <input
          type="checkbox"
          v-model="showLayer2"
          id="default-toggle2"
          class="sr-only peer"
        />
        <div
          class="w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-blue-600"
        ></div>
        <span class="ml-3 text-sm font-medium">Tools</span>
      </label>
      <label
        for="default-toggle3"
        class="inline-flex relative items-center cursor-pointer"
      >
        <input
          type="checkbox"
          v-model="showLayer3"
          id="default-toggle3"
          class="sr-only peer"
        />
        <div
          class="w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-blue-600"
        ></div>
        <span class="ml-3 text-sm font-medium">Back-end?</span>
      </label>
      <label
        for="default-toggle4"
        class="inline-flex relative items-center cursor-pointer"
      >
        <input
          type="checkbox"
          v-model="showLayer4"
          id="default-toggle4"
          class="sr-only peer"
        />
        <div
          class="w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-blue-600"
        ></div>
        <span class="ml-3 text-sm font-medium">Hidden😁?</span>
      </label>
    </div>
  </div>
</template>


<style scoped>
.card{
  height: 30rem;
  width: 28rem;
}
@media only screen and (max-width: 620px) {
  .card{
    width: 90vw;
    height: 90vw+1rem;
    border: solid red 3px;
  }
}
.enter-active,
.leave-active {
  transition: opacity 0.5s ease;
}

.enter-from,
.leave-to {
  opacity: 0;
}
</style>