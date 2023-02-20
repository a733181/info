<template>
  <div id="home">
    <p
      v-if="load !== 100"
      class="text-white text-9xl z-40 absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2"
      :style="opacityHiddenStyle"
    >
      {{ loadText }}
    </p>
    <div class="hero">
      <h1 class="text-white text-9xl mb-20" :style="opacityShowStyle">SYUAN</h1>
      <a href="#about" class="block cursor-pointer hover:opacity-60">
        <img
          src="@/assets/svg/arrow-down-solid.svg"
          alt="arrow"
          class="w-20"
          :class="{ 'animate-bounce': load >= 50 }"
        />
      </a>
    </div>
    <div
      v-if="load !== 100"
      class="bg-black z-30 fixed top-0 left-0 right-0 bottom-0 duration-75"
      :style="opacityHiddenStyle"
    ></div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const loadText = ref('0%');

const load = ref(0);

const scale = (number, inMin, inMax, outMin, outMax) => {
  return ((number - inMin) * (outMax - outMin)) / (inMax - inMin) + outMin;
};

const blurring = () => {
  load.value++;
  if (load.value > 99) {
    clearInterval(setTime);
  }
  loadText.value = `${load.value}%`;
};

const setTime = setInterval(blurring, 50);

const opacityHiddenStyle = computed(() => {
  return `opacity:${scale(load.value, 0, 100, 1, 0)}`;
});

const opacityShowStyle = computed(() => {
  return `opacity:${scale(load.value, 100, 0, 1, 0)}`;
});
</script>

<style scoped>
.hero {
  background: url('../assets/img/hero.png') no-repeat center / cover;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 2rem;
}
</style>
