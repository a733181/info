<template>
  <section id="work">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">工作經驗</h2>
    <ul class="lg:w-1/2 mx-auto">
      <li class="dot">
        <div class="bg-white p-6 shadow-sm rounded-2xl">
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
        <div class="bg-white p-6 shadow-sm rounded-2xl">
          <p
            class="text-white bg-primary text-lg inline-block py-2 px-4 rounded-lg"
          >
            2018 - 2021
          </p>
          <h3 class="text-4xl font-bold py-3">喬宣有限公司</h3>
          <p class="mb-3 ml-3">業務助理 新北市永和區</p>
          <ul class="list-decimal ml-6 space-y-3">
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
        <div class="bg-white p-6 shadow-sm rounded-2xl">
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
</template>

<style scoped>
.dot {
  @apply border-l-2 pl-8 border-primary relative pb-6;
}
.dot:before {
  @apply content-[''] absolute top-0 bg-primary w-8 h-8 -left-4 rounded-full;
}
</style>
