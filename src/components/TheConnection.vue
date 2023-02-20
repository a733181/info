<template>
  <section id="connection">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">聯絡我</h2>
    <form
      action="https://docs.google.com/forms/u/0/d/e/1FAIpQLSfaKgy30vw1weSSfS2AASObus_v03iF2nQ5zVK0WSy7Eo0keg/formResponse"
      method="POST"
      class="text-3xl bg-white shadow-sm flex flex-col gap-10 py-20 lg:px-40 rounded-lg lg:w-1/2 lg:mx-auto"
    >
      <input
        type="text"
        name="entry.1270831185"
        placeholder="姓名&ensp;/&ensp;稱呼"
        class="outline-none focus:border-primary border-2 w-11/12 mx-auto p-4 rounded-lg"
        required
      />

      <input
        type="connection"
        name="entry.389397974"
        placeholder="聯絡方式"
        class="outline-none focus:border-primary w-11/12 mx-auto border-2 p-4 rounded-lg"
        required
      />

      <textarea
        id="message"
        name="entry.1600714924"
        placeholder="訊息"
        class="outline-none focus:border-primary w-11/12 mx-auto border-2 p-4 rounded-lg h-96"
        required
      ></textarea>
      <div class="flex gap-8 items-center justify-center">
        <button
          type="reset"
          class="border-2 rounded-lg py-4 px-6 border-primary text-primary hover:bg-primary hover:text-white duration-200"
        >
          清除
        </button>
        <button
          type="submit"
          class="border-2 rounded-lg py-4 px-6 text-white bg-primary border-primary first-letter hover:bg-white hover:text-primary duration-200"
        >
          送出
        </button>
      </div>
    </form>
  </section>
</template>

<script setup>
import { reactive } from 'vue';
import axios from 'axios';

const form = reactive({
  name: '',
  connection: '',
  message: '',
});

const submitHandler = async () => {
  try {
    const url =
      'https://docs.google.com/forms/u/0/d/e/1FAIpQLSfaKgy30vw1weSSfS2AASObus_v03iF2nQ5zVK0WSy7Eo0keg/formResponse';
    await axios.post(url, {
      'entry.1270831185': form.name,
      'entry.389397974': form.connection,
      'entry.1600714924': form.message,
    });
  } catch (error) {
    console.log(error);
  }
};
</script>
