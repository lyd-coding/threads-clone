<template>
  <div class="bg-black fixed w-[calc(100%+1px)] h-full">
    <NuxtPage />

    <CreatePost :class="[
      { 'max-h-[100vh] transition-all duration-200 ease-in visible': userStore.isMenuOverlay },
      { 'max-h-0 transition-all duration-200 ease-out invisible': !userStore.isMenuOverlay }
    ]"></CreatePost>
  </div>
</template>

<script setup>
import { useUserStore } from './stores/user';

const userStore = useUserStore();
</script>
