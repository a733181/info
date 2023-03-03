<template>
  <div class="bg-white shadow-sm">
    <div class="card border-[1rem] border-white h-[30rem] rounded-lg">
      <a :href="props.item.page" target="_blank">
        <img
          :src="props.item.img"
          :alt="props.item.title"
          class="w-full h-[88%] object-cover object-top mb-6 hover:scale-110 duration-150"
        />
      </a>
      <h2 class="text-3xl bottom-0 left-0 font-bold">
        {{ props.item.title }}
      </h2>
    </div>
    <div v-if="item.describe" class="px-6 py-7 mt-4">
      <p class="whitespace-pre-line mb-6 text-2xl">{{ item.describe }}</p>
      <h3 class="font-bold mb-2">使用技術</h3>
      <ul class="list-disc ml-8 flex flex-wrap">
        <li v-for="(skill, index) in item.skill" :key="index" class="w-1/3">
          {{ skill }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  item: {
    type: Object,
    default: {},
  },
});
</script>

<style scoped></style>
