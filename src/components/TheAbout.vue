<template>
  <section id="about">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">關於我</h2>
    <div class="flex gap-6 flex-col lg:flex-row lg:justify-center">
      <img
        src="@/assets/img/syuan.jpg"
        alt="syuan"
        class="w-[300px] lg:w-1/4 border-4 border-primary rounded-xl h-full lg:mr-10 mx-auto lg:mx-0"
      />
      <div>
        <h3 class="text-gray-800 font-bold text-6xl mb-4">黃姿瑄</h3>
        <h4 class="text-xl">中華科技大學-資訊管理學系 2009~2013</h4>
        <p class="mb-8 text-xl"></p>
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
        <form
          action="https://docs.google.com/forms/d/e/1FAIpQLSfaKgy30vw1weSSfS2AASObus_v03iF2nQ5zVK0WSy7Eo0keg/viewform"
          method="POST"
          class="text-3xl bg-white shadow-sm flex flex-col gap-10 py-10 rounded-lg"
        >
          <input
            type="text"
            placeholder="姓名&ensp;/&ensp;稱呼"
            class="outline-none focus:border-primary border-2 w-11/12 mx-auto p-4 rounded-lg"
          />

          <input
            type="connection"
            placeholder="聯絡方式"
            class="outline-none focus:border-primary w-11/12 mx-auto border-2 p-4 rounded-lg"
          />

          <textarea
            id="message"
            placeholder="訊息"
            class="outline-none focus:border-primary w-11/12 mx-auto border-2 p-4 rounded-lg h-96"
          ></textarea>
          <button type="reset">清除</button>
          <button type="submit">送出</button>
        </form>
      </div>
    </div>
  </section>
</template>
