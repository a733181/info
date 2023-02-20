<template>
  <section id="portfolio">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">作品集</h2>
    <div class="grid lg:grid-cols-4 gap-10">
      <Card v-for="(item, index) in portfolio" :key="index" :item="item" />
    </div>
  </section>
</template>

<script setup>
import Card from '@/components/TheCard.vue';

const portfolio = [
  {
    title: 'Vue 團購網',
    img: new URL('@/assets/img/vue-buytogether.jpg', import.meta.url).href,
    github: 'https://github.com/a733181/2022-buytogether',
    page: 'https://a733181.github.io/2022-buytogether/#/',
  },
  {
    title: 'Vue 番茄鐘',
    img: new URL('@/assets/img/vue-pomodoro.jpg', import.meta.url).href,
    github: 'https://github.com/a733181/2022-Vue-Pomodoro',
    page: 'https://a733181.github.io/2022-Vue-Pomodoro/#/',
  },
  {
    title: 'line機器人 搜尋食譜',
    img: new URL('@/assets/img/node-line-bot.jpg', import.meta.url).href,
    github: 'https://github.com/a733181/2022-nodeLineBot-recipe',
    page: 'LINE ID：@599emgee',
  },
  {
    title: '90秒小遊戲',
    img: new URL('@/assets/img/js-jq-game.jpg', import.meta.url).href,
    github: 'https://github.com/a733181/2022-jq-canvas-game',
    page: 'https://a733181.github.io/2022-jq-canvas-game/',
  },
  {
    title: 'Countries-API',
    img: new URL('@/assets/img/js-countries-api.jpg', import.meta.url).href,
    github:
      'https://github.com/a733181/frontendMentor-REST-Countries-API-with-color-theme-switcher',
    page: 'https://a733181.github.io/frontendMentor-REST-Countries-API-with-color-theme-switcher/',
  },
  {
    title: '井字棋',
    img: new URL('@/assets/img/js-tic-tac-toe.jpg', import.meta.url).href,
    github: 'https://github.com/a733181/2022-js-tic-tac-toe',
    page: 'https://a733181.github.io/2022-js-tic-tac-toe/',
  },
  {
    title: '卡片翻牌遊戲',
    img: new URL('@/assets/img/js-memory-game.jpg', import.meta.url).href,
    github: 'https://github.com/a733181/2022-jq-memory-game',
    page: 'https://a733181.github.io/2022-jq-memory-game/',
  },
  {
    title: '萬年曆',
    img: new URL('@/assets/img/js-calendar.jpg', import.meta.url).href,
    github: 'https://github.com/a733181/2022-js-calendar',
    page: 'https://a733181.github.io/2022-js-calendar/',
  },
  {
    title: '時鐘',
    img: new URL('@/assets/img/js-clock.jpg', import.meta.url).href,
    github: 'https://github.com/a733181/2022-js-clock',
    page: 'https://a733181.github.io/2022-js-clock/',
  },
  {
    title: '音樂撥放器',
    img: new URL('@/assets/img/js-music-play.jpg', import.meta.url).href,
    github:
      'https://github.com/a733181/frontendMentor-REST-Countries-API-with-color-theme-switcher',
    page: 'https://a733181.github.io/2021-practice-music_play/',
  },
];
</script>
