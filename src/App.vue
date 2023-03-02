<template>
  <div class="overflow-hidden">
    <Header />
    <Home />
    <About />
    <Skill />
    <Portfolio />
    <Work />
    <Connection />
  </div>
</template>

<script setup>
import { ref, provide } from 'vue';

import Header from '@/components/TheHeader.vue';
import Home from '@/components/TheHome.vue';
import About from '@/components/TheAbout.vue';
import Skill from '@/components/TheSkill.vue';
import Portfolio from '@/components/ThePortfolio.vue';
import Work from '@/components/TheWork.vue';
import Connection from './components/TheConnection.vue';

const toggleHeader = ref(false);

provide('toggleHeader', toggleHeader);
</script>

<style>
html {
  @apply text-[62.5%] scroll-smooth;
}

body {
  @apply duration-200 bg-[#fcf2e8];
}

section {
  @apply min-h-[100vh] px-[5%] py-8 lg:ml-[30rem];
}
</style>
