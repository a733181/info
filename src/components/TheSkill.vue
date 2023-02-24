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
      '使用 Vite 建立 Vue 專案並設定開發環境',
      '能夠使用 Vue-Router 建立路由頁面並實現動態路由配置',
      '在 Vue 中安裝及使用第三方套件以擴展功能',
      '具備使用 components 管理元件並提高代碼重複使用性的能力',
      '使用 Pinia 狀態管理庫集中管理 Vue 專案中的資料',
    ],
  },
  {
    title: 'Node',
    list: [
      '能夠使用 Express 建立伺服器並實現路由配置',
      '使用 CORS 跨域資源共用',
      '使用 Mongoose 連接 MongoDB 資料庫，進行 CRUD 操作',
      '具備建立 API 串接前端的能力，提供合適的數據接口',
    ],
  },
  {
    title: 'JavaScript',
    list: [
      '使用 ES6 ，並應用其特性進行開發',
      '能夠使用 AJAX / JSON 串接 API，實現前後端數據交互',
      '使用 jQuery 函式庫的能力，提高代碼編寫效率',
    ],
  },
  {
    title: 'Web / Layout',
    list: [
      '了解並應用自適應網頁設計 RWD',
      '使用 SASS 預處理器進行 CSS 編寫',
      '使用 Bootstrap 5 和 Tailwind CSS 進行切版',
      '使用 GitHub Page 部屬專案，實現線上展示',
    ],
  },
];
</script>
