<template>
  <section id="work">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">工作經驗</h2>
    <ul class="lg:w-1/2 mx-auto">
      <li class="dot" v-for="(job, index) in jobs" :key="index">
        <div class="bg-white p-6 shadow-sm rounded-2xl">
          <p
            class="text-white bg-primary text-lg inline-block py-2 px-4 rounded-lg"
          >
            {{ job.worKDate }}
          </p>
          <h3 class="text-4xl font-bold py-3">
            {{ job.company }}
          </h3>
          <p class="mb-3">{{ job.jobTitle }} {{ job.area }}</p>
          <p class="text-xl whitespace-pre-line leading-relaxed">
            {{ job.content }}
          </p>
        </div>
      </li>
    </ul>
  </section>
</template>

<script setup>
const jobs = [
  {
    company: '前端網頁開發技術(青年專班)(泰山)-課程',
    worKDate: '2022-2023',
    jobTitle: '',
    area: '新北市泰山區',
    content: '',
  },
  {
    company: '喬宣有限公司',
    worKDate: '2018 - 2021',
    jobTitle: '業務助理',
    area: '新北市永和區',
    content:
      '負責通路後台商品管理、訂單處理、客訴及退換貨處理，以及電話和線上客服。\n同時，還負責統計整理銷售數量並進行庫存管理。工作內容多元且相當細膩，達到了良好的表現。',
  },
  {
    company: '多必優國際有限公司',
    jobTitle: '行政助理',
    area: '新北市新莊區',
    content: '',
  },
];
</script>

<style scoped>
.dot {
  @apply border-l-2 pl-8 border-primary relative pb-6;
}
.dot:before {
  @apply content-[''] absolute top-0 bg-primary w-8 h-8 -left-4 rounded-full;
}
</style>
