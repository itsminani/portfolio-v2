<script setup lang="ts">
import {useDark, useToggle} from "@vueuse/core"

const isDark = useDark()
const toggleDark = useToggle(isDark)
</script>

<template>
    <button class="round" @click="toggleDark()">{{ isDark?"☀️":"🌙"}}</button>
</template>


