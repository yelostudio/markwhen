<script setup lang="ts">
import { useTimelineStore } from "../timelineStore";

const timelineStore = useTimelineStore();

const toggleHideNowLine = () => {
  timelineStore.setHideNowLine(!timelineStore.hideNowLine);
};
</script>

<template>
  <button
    class="h-6 flex flex-row items-center rounded hover:bg-zinc-200 transition dark:border-gray-900 dark:hover:bg-gray-900 dark:hover:text-gray-100 px-1 text-sm lg:text-base font-bold"
    title="Toggle now line"
    @click="toggleHideNowLine"
  >
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="1 2 17 12" class="h-5 w-5">
      <path
        d="m 2 3 a 1 1 0 0 0 0 2 h 11 a 1 1 0 1 0 0 -2 h -11 z m 1 4 a 1 1 0 0 0 0 2 h 11 a 1 1 0 0 0 0 -2 h -11 z m 1 4 a 1 1 0 1 0 0 2 h 11 a 1 1 0 1 0 0 -2 h -11 z"
        fill="currentColor"
      />
      <path d="M 9 1 L 9 15 L 11 15 L 11 1 L 11 1 Z" fill="currentColor"></path>
    </svg>
  </button>
</template>

<style scoped></style>
