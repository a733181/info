<template>
  <section id="about">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">關於我</h2>
    <div class="flex gap-6 flex-col lg:flex-row lg:justify-center">
      <img
        src="@/assets/img/syuan.jpg"
        alt="syuan"
        class="w-[300px] lg:w-1/4 border-4 border-primary rounded-xl h-full lg:mr-10 mx-auto lg:mx-0"
      />
      <div class="lg:w-1/2">
        <h3 class="text-gray-800 font-bold text-6xl mb-4">黃姿瑄</h3>
        <h4 class="text-xl mb-16">中華科技大學-資訊管理學系 2009~2013</h4>
        <div class="mb-16">
          <h2 class="text-4xl font-bold mb-4">自傳</h2>
          <p class="mb-6 text-2xl">
            您好，我是黃姿瑄，具七年資訊助理工作經驗，在工作中使用 WordPress
            重購公司品牌官網，發現自己對於網頁設計相關技術有濃厚的興趣，在自學期間學習
            HTML、CSS及 JavaScript ，後續參與半年的專業訓練，進一步掌握
            Bootstrap、Vue.js、Node.js 與 MongoDB
            等前端開發技術，能獨立建置一個具前後台功能的主題官網，並可使用 Git
            版本控制進行管理。
            前端開發技術日新月異，唯有不斷的學習才能與時俱進，而我將持續精進
            JavaScript
            與相關框架的運用，希望能為公司及團隊帶來價值，成為獨當一面的前端工程師。
          </p>
          <a
            class="text-2xl ml-auto block bg-white py-2 rounded-lg text-primary hover:opacity-60 w-[100px] text-center shadow-sm"
            href="#portfolio"
            >作品集</a
          >
        </div>
        <div class="flex gap-10 flex-col lg:flex-row mb-10">
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
</template>
