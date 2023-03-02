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
          <p class="text-2xl whitespace-pre-line leading-relaxed">
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
    company: '喬宣有限公司',
    worKDate: '2018 - 2021',
    jobTitle: '業務助理',
    area: '新北市永和區',
    content:
      '1.負責運用 WordPress 開發公司品牌官網。\n2.負責 ERP 系統操作及 CRM 客戶關係管理。\n3.負責商品管理與銷售數據統計分析。',
  },
  {
    company: '多必優國際有限公司',
    worKDate: '2014 - 2017',
    jobTitle: '行政助理',
    area: '新北市新莊區',
    content:
      '1.負責商品採購及行政事務。\n2.負責商品進銷存和客戶關係管理。\n3.負責商品管理與銷售數據統計分析。',
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
