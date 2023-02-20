<template>
  <section id="skill">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">技能</h2>
    <ul class="flex flex-wrap gap-10 justify-center">
      <li
        class="w-full lg:w-1/3 bg-white py-10 px-12 rounded-xl shadow-sm"
        v-for="(item, itemIndex) in skill"
        :key="itemIndex"
      >
        <h2 class="text-4xl mb-8 font-bold">{{ item.title }}</h2>
        <ol class="list-disc ml-8">
          <li
            v-for="(text, textIndex) in item.list"
            :key="textIndex"
            class="text-2xl mb-4"
          >
            {{ text }}
          </li>
        </ol>
      </li>
    </ul>
  </section>
</template>

<script setup>
const skill = [
  {
    title: 'Vue',
    list: [
      '使用 Vite 建立 Vue',
      '使用 Vue-Router 建立路由',
      '在 Vue 安裝及使用第三方套件',
      '使用 components 管理元件',
      '使用 Pinia 集中管理資料',
    ],
  },
  {
    title: 'Node',
    list: [
      '使用 Express 建立伺服器',
      '使用 CORS 跨域資源共用',
      '使用 Mongoose 連接 MongoDB 資料庫',
      '建立 API 串接前端',
    ],
  },
  {
    title: 'JavaScript',
    list: ['了解 並會使用 ES6 語言', '通過 AJAX / JSON 串接 API'],
  },
  {
    title: 'Web / Layout',
    list: [
      '了解 自適應網頁設計 RWD',
      '了解 SASS 預處理器',
      '了解  Bootstrap 5 並應用元件',
      '了解 Tailwind CSS',
      'GitHub Page 部屬',
    ],
  },
];
</script>
