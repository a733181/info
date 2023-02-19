<template>
  <div class="">
    <div
      class="fixed z-20 bg-primary cursor-pointer top-4 right-4 px-5 py-4 rounded-lg block lg:hidden"
    >
      <img
        src="@/assets/bars-solid.svg"
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
          class="duration-200 hover:text-primary hover:tracking-wider"
          href="#home"
          @click="toggleHeader = !toggleHeader"
          >首頁</a
        >
        <a
          class="duration-200 hover:text-primary hover:tracking-wider"
          href="#about"
          @click="toggleHeader = !toggleHeader"
          >關於我</a
        >
        <a
          class="duration-200 hover:text-primary hover:tracking-wider"
          href="#skill"
          @click="toggleHeader = !toggleHeader"
          >技能</a
        >
        <a
          class="duration-200 hover:text-primary hover:tracking-wider"
          href="#portfolio"
          @click="toggleHeader = !toggleHeader"
          >作品集</a
        >
        <a
          class="duration-200 hover:text-primary hover:tracking-wider"
          href="#work"
          @click="toggleHeader = !toggleHeader"
          >工作經驗</a
        >
      </nav>
      <div class="flex justify-center items-center gap-5">
        <a
          href="https://github.com/a733181"
          class="hover:opacity-60 duration-150"
        >
          <img src="@/assets/github.svg" alt="github" class="w-9" />
        </a>
        <a
          href="https://discord.com/users/SYUAN#7156"
          class="hover:opacity-60 duration-150"
        >
          <img src="@/assets/discord.svg" alt="discord" class="w-10" />
        </a>
        <a
          href="https://line.me/ti/p/mZnErV_2XK"
          class="hover:opacity-60 duration-150"
        >
          <img src="@/assets/line.svg" alt="line" class="w-9" />
        </a>
        <a href="mailto:a733181@gmail.com">
          <img src="@/assets/envelope-solid.svg" alt="email" class="w-9" />
        </a>
      </div>
    </header>
    <section id="home"></section>
    <section id="about">
      <h2 class="text-6xl mb-10 lg:mb-20 mt-2 font-bold">關於我</h2>
      <div class="flex gap-6 flex-col lg:flex-row lg:justify-center">
        <img
          src="./assets/syuan.jpg"
          alt="syuan"
          class="w-[300px] lg:w-1/4 border-4 border-primary rounded-xl h-full lg:mr-10 mx-auto lg:mx-0"
        />
        <div>
          <h3 class="text-gray-800 font-bold text-6xl mb-4">黃姿瑄</h3>
          <h4 class="text-xl">中華科技大學-資訊管理學系 2009~2013</h4>
          <p class="mb-8 text-xl"></p>
          <div class="flex gap-10 flex-col lg:flex-row">
            <div>
              <h4 class="text-4xl font-bold">求職資訊</h4>
              <table class="text-3xl text-gray-700 table-auto">
                <tr class="pb-10">
                  <td class="text-primary py-4 w-[100px]">求職地點：</td>
                  <td class="py-4">台北市、新北市</td>
                </tr>
                <tr>
                  <td class="text-primary w-[100px] py-4">求職職稱：</td>
                  <td class="py-4">前端工程師</td>
                </tr>
              </table>
            </div>
            <div>
              <h4 class="text-4xl font-bold">聯絡方式</h4>
              <table class="text-3xl text-gray-700 table-auto">
                <tr class="pb-10">
                  <td class="text-primary py-4 w-[100px]">Email：</td>
                  <td class="py-4">
                    <a
                      href="mailto:a733181@gmail.com"
                      class="hover:opacity-60 duration-150"
                      >a733181@gmail.com</a
                    >
                  </td>
                </tr>
                <tr>
                  <td class="text-primary w-[100px] py-4">Line：</td>
                  <td class="py-4">
                    <a
                      href="https://line.me/ti/p/mZnErV_2XK"
                      class="hover:opacity-60 duration-150"
                      >1tm3dth5</a
                    >
                  </td>
                </tr>
                <tr>
                  <td class="text-primary w-[100px] py-4">Discord：</td>
                  <td class="py-4">
                    <a
                      href="https://discord.com/users/SYUAN#7156"
                      class="hover:op-60 duration-150"
                      >SYUAN#7156</a
                    >
                  </td>
                </tr>
              </table>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section id="skill">
      <h2 class="text-6xl mb-10 lg:mb-20 mt-2 font-bold">技能</h2>
    </section>
    <section id="portfolio">
      <h2 class="text-6xl mb-10 lg:mb-20 mt-2 font-bold">作品集</h2>
    </section>
    <section id="work">
      <h2 class="text-6xl mb-10 lg:mb-20 mt-2 font-bold">工作經驗</h2>
      <ul class="lg:w-1/2 mx-auto">
        <li class="dot">
          <div class="bg-white p-6 shadow-md shadow-orange-100 rounded-2xl">
            <p
              class="text-white bg-primary text-lg inline-block py-2 px-4 rounded-lg"
            >
              2022-2023
            </p>
            <h3 class="text-4xl font-bold py-3">
              前端網頁開發技術(青年專班)(泰山)
            </h3>
            <p class="mb-3 ml-3">新北市泰山區</p>
          </div>
        </li>
        <li class="dot">
          <div class="bg-white p-6 shadow-md shadow-orange-100 rounded-2xl">
            <p
              class="text-white bg-primary text-lg inline-block py-2 px-4 rounded-lg"
            >
              2018 - 2021
            </p>
            <h3 class="text-4xl font-bold py-3">喬宣有限公司</h3>
            <p class="mb-3 ml-3">業務助理 新北市永和區</p>
            <ul class="list-decimal ml-3 space-y-3">
              <li class="text-2xl">通路後台商品管理</li>
              <li class="text-2xl">訂單處理。</li>
              <li class="text-2xl">客訴處理、退換貨處理。</li>
              <li class="text-2xl">電話客服及線上客服。</li>
              <li class="text-2xl">統計整理銷售數量。</li>
              <li class="text-2xl">庫存管理。</li>
            </ul>
          </div>
        </li>
        <li class="dot">
          <div class="bg-white p-6 shadow-md shadow-orange-100 rounded-2xl">
            <p
              class="text-white bg-primary text-lg inline-block py-2 px-4 rounded-lg"
            >
              2014 - 2017
            </p>
            <h3 class="text-4xl font-bold py-3">多必優國際有限公司</h3>
            <p class="mb-3 ml-3">行政助理 新北市新莊區</p>
          </div>
        </li>
      </ul>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const toggleHeader = ref(false);
</script>

<style>
html {
  @apply text-[62.5%] scroll-smooth;
}

body {
  @apply duration-200 bg-[#fcf2e8];
}

section {
  @apply min-h-[100vh] px-[5%] py-4 lg:ml-[30rem];
}

.dot {
  @apply border-l-2 pl-8 border-primary relative pb-6;
}
.dot:before {
  @apply content-[''] absolute top-0 bg-primary w-8 h-8 -left-4 rounded-full;
}
</style>
