<template>
  <section id="skill">
    <h2 class="text-6xl my-10 lg:mb-20 font-bold">技能</h2>
    <ul class="flex flex-wrap gap-10 justify-center">
      <li
        class="w-full lg:w-1/4 bg-white py-10 px-12 rounded-xl shadow-sm"
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
    title: '前端',
    list: [
      'HTML',
      'CSS',
      'SCSS / SASS',
      'Bootstrap',
      'Tailwind CSS',
      'JavaScript',
      'jQuery',
      'Vue.js',
    ],
  },
  {
    title: '後端',
    list: ['Node', 'MongoDB'],
  },
  {
    title: '其他',
    list: ['Git 版本控制'],
  },
];
</script>
