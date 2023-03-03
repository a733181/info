<template>
  <div>
    <div
      class="fixed z-20 bg-primary cursor-pointer top-4 right-4 px-5 py-4 rounded-lg block lg:hidden"
    >
      <img
        src="@/assets/svg/bars-solid.svg"
        alt="bars"
        class="w-6"
        @click="toggleHeader = !toggleHeader"
      />
    </div>

    <header
      class="bg-gray-900 fixed top-0 left-0 bottom-0 w-full lg:w-[30rem] flex flex-col py-32 px-8 -translate-y-full lg:translate-y-0 duration-300 z-10"
      :class="{ 'translate-y-0': toggleHeader }"
    >
      <h1 class="text-primary text-5xl font-bold mb-20 text-center">Syuan</h1>
      <nav
        class="text-white flex flex-col text-3xl space-y-9 items-center mb-20"
      >
        <a
          v-for="(item, index) in nav"
          :key="index"
          class="duration-200 hover:text-primary hover:tracking-wider"
          :href="item.link"
          @click="toggleHeader = !toggleHeader"
          >{{ item.title }}</a
        >
      </nav>
      <div class="flex justify-center items-center gap-5">
        <a
          href="https://github.com/a733181"
          class="hover:opacity-60 duration-150"
        >
          <img src="@/assets/svg/github.svg" alt="github" class="w-9" />
        </a>
        <a
          href="https://discord.com/users/SYUAN#7156"
          class="hover:opacity-60 duration-150"
        >
          <img src="@/assets/svg/discord.svg" alt="discord" class="w-10" />
        </a>
        <a href="mailto:a733181@gmail.com">
          <img
            src="@/assets/svg/envelope-solid.svg"
            alt="email"
            class="w-9 hover:opacity-60 duration-150"
          />
        </a>
      </div>
    </header>
  </div>
</template>

<script setup>
import { inject } from 'vue';

const toggleHeader = inject('toggleHeader');

const nav = [
  {
    title: '首頁',
    link: '#home',
  },
  {
    title: '關於我',
    link: '#about',
  },
  {
    title: '技能',
    link: '#skill',
  },
  {
    title: '作品集',
    link: '#portfolio',
  },
  {
    title: '工作經驗',
    link: '#work',
  },
  { title: '聯絡我', link: '#connection' },
];
</script>
