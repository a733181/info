<template>
  <section id="portfolio">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">作品集</h2>
    <div class="mb-20">
      <a
        :href="project.page"
        target="_blank"
        class="block lg:w-2/3 order-1 lg:order-2 hover:opacity-60 duration-150"
      >
        <h3 class="text-4xl font-bold mb-6">
          專題&ensp;|&ensp;{{ project.title }}
        </h3>
      </a>
      <div class="flex items-center gap-10 flex-col lg:flex-row mb-10">
        <div class="mb-6 lg:w-1/3 order-2 lg:order-1">
          <h4 class="text-3xl font-bold mb-6">專案發想</h4>
          <p class="text-2xl leading-[1.8]">{{ project.describe }}</p>
        </div>
        <a
          :href="project.page"
          target="_blank"
          class="block lg:w-2/3 order-1 lg:order-2 hover:opacity-60 duration-150"
        >
          <img :src="project.img" :alt="project.title" />
        </a>
      </div>
      <div class="flex flex-wrap space-y-6">
        <div class="grid lg:grid-cols-3 gap-10">
          <img v-for="(img, index) in project.images" :key="index" :src="img" />
        </div>
        <div class="lg:w-[49%]">
          <h4 class="text-3xl mb-6">前端技術</h4>
          <ul class="list-disc ml-6 text-2xl space-y-2">
            <li v-for="(skill, index) in project.frontSkill" :key="index">
              {{ skill }}
            </li>
          </ul>
        </div>
        <div class="lg:w-[49%]">
          <h4 class="text-3xl mb-6">後端技術</h4>
          <ul class="list-disc ml-6 text-2xl space-y-2">
            <li v-for="(skill, index) in project.backSkill" :key="index">
              {{ skill }}
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="grid lg:grid-cols-3 gap-10">
      <Card v-for="(item, index) in portfolio" :key="index" :item="item" />
    </div>
  </section>
</template>

<script setup>
import Card from '@/components/TheCard.vue';

const project = {
  title: '團購趣',
  img: new URL('@/assets/img/vue-buytogether.jpg', import.meta.url).href,
  images: [
    new URL('@/assets/img/vue-buytogether01.jpg', import.meta.url).href,
    new URL('@/assets/img/vue-buytogether02.jpg', import.meta.url).href,
    new URL('@/assets/img/vue-buytogether03.jpg', import.meta.url).href,
  ],
  github: 'https://github.com/a733181/2022-buytogether',
  page: 'https://a733181.github.io/2022-buytogether/#/',
  describe:
    '團購網的設計目的在於解決社交媒體上進行團購時，團主面臨的商品管理、訂單統計、與團員反覆溝通等問題。\n希望透過一個線上團購平台，提供一個便利的解決方案，讓團主可以輕鬆管理商品及訂單，團員也能夠隨時查看商品狀態。\n透過平台，我們希望可以簡化團購過程，讓團購變得更加方便、流暢和輕鬆。我們的目標是提供一個方便、高效的團購平台，讓團主和團員可以更加專注於團購本身，並獲得更好的團購體驗。',
  frontSkill: [
    '使用 Vite 搭建開發環境，Vue 作為主要框架，Vue-router 管理路由，Pinia 集中管理資料狀態。',
    '整合 ESLint、Axios、Swiper、Vue-Chartjs、SweetAlert2、Validator、Socket.io、Tailwind CSS、GSAP 等第三方套件，增強功能和提升使用體驗。',
    '使用 ESLint 做程式碼檢查，確保程式碼符合規範。',
    '使用 Axios 處理 API 請求。',
    '使用 Swiper 製作商品輪播圖。',
    '使用 vue-chartjs 製作後台購買及銷售訂單圖表。',
    '使用 SweetAlert2 提供新增、修改成功跟新增、修改、刪除錯誤等等提示。',
    '使用 Validator 驗證表單資料。',
    '使用 Socket.io 製作私訊聊天室，讓團主與團員溝通更加流暢。',
    '使用 Tailwind CSS 為 CSS 框架。',
    '使用 GSAP 製作動畫及視差滾動效果。',
  ],
  backSkill: [
    '使用 node.js express 建立伺服器。',
    '整合 ESLint、Bcrypt、Cloudinary、Cors、Mongoose、Multer、Passport、Socket.io、Validator 等第三方套件，增強功能和提升使用體驗。',
    '使用 ESLint 做程式碼檢查，確保程式碼符合規範。',
    '使用 Mongoose 連接 MongoDB 資料庫。',
    '使用 Bcrypt 密碼加密。',
    '使用 Passport 比對登入密碼。',
    '使用 Validator 驗證輸入資料。',
    '使用 Multer 上傳圖片至 Cloudinary。',
    '使用 Socket.io 製作私訊聊天室',
    '使用 Cors 解決資源跨域。',
  ],
};
const portfolio = [
  {
    title: '鄭嘉琪醫生 形象官網',
    img: new URL('../assets/img/dreamuTW.jpg', import.meta.url).href,
    page: 'https://www.dreamutw.com/',
    describe:
      '與平面設計師合作製鄧醫生個人形象官網，展現了醫生的專業形象，為客戶提供清晰和實用的資訊',
    skill: ['Vue.js'],
  },
  {
    title: '番茄鐘',
    img: new URL('@/assets/img/vue-pomodoro.jpg', import.meta.url).href,
    page: 'https://a733181.github.io/2022-Vue-Pomodoro/#/',
    describe:
      '使用番茄鐘讓您更加專注於任務。\n設定您的工作時間和休息時間，按下開始按鈕，番茄鐘就會自動開始計時。當時間結束，您將收到提示音，提醒您休息或開始下一個番茄鐘。\n透過這個工具，您可以更加高效地完成工作，達成自己的目標。',
    skill: ['Vite', 'Vue.js', 'Vuetify', 'Pinia', 'Pug', 'Sass', 'Eslint'],
  },
  {
    title: '機器人 搜尋食譜',
    img: new URL('@/assets/img/node-line-bot.jpg', import.meta.url).href,
    page: 'https://lin.ee/5nSlCrD',
    describe:
      '食譜搜尋小幫手！只需要輸入您想要的食材或菜名，我們就會幫您找到相關的食譜。',
    skill: ['Node.js', 'Axios', 'Cheerio', 'Linebot', 'Eslint'],
  },
  {
    title: '90秒小遊戲',
    img: new URL('@/assets/img/js-jq-game.jpg', import.meta.url).href,
    page: 'https://a733181.github.io/2022-jq-canvas-game/',
    describe:
      '在這個遊戲中，您需要使用鍵盤來控制角色的移動，按下 F 鍵來攻擊怪物。\n您需要時刻保持警惕，因為怪物可能會出現在任何地方。',
    skill: ['jQuery', 'JavaScript', 'CSS'],
  },
  {
    title: '卡片翻牌遊戲',
    img: new URL('@/assets/img/js-memory-game.jpg', import.meta.url).href,
    page: 'https://a733181.github.io/2022-jq-memory-game/',
    describe:
      '遊戲開始！讓你的記憶力和觀察力得到挑戰。通過翻開卡片，找出相同的圖案，完成所有的匹配。遊戲有多種難度供你選擇，保證讓你愉快地度過每一個時刻。快來嘗試這個具有挑戰性和趣味性的翻牌遊戲，讓你享受遊戲的樂趣！',
    skill: ['jQuery', 'JavaScript', 'CSS'],
  },
  {
    title: '井字棋',
    img: new URL('@/assets/img/js-tic-tac-toe.jpg', import.meta.url).href,
    page: 'https://a733181.github.io/2022-js-tic-tac-toe/',
    describe:
      '透過這個網頁，你和你的朋友可以隨時隨地享受井字棋的樂趣！只要打開網頁，立即展開對戰。不論是想放鬆休閒還是挑戰自我，都能在這個簡單又有趣的遊戲中找到樂趣。趕快來一局吧！',
    skill: ['JavaScript', 'CSS'],
  },
];
</script>
