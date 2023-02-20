<template>
  <div
    class="card border-[1rem] shadow-sm border-white bg-white h-[25rem] relative rounded-lg"
  >
    <img
      :src="props.item.img"
      :alt="props.item.title"
      class="img w-full h-full object-cover object-left-top relative z-[1]"
    />
    <h2 class="absolute text-3xl bottom-0 left-0 font-bold">
      {{ props.item.title }}
    </h2>
    <div class="absolute top-2 right-0 space-y-5">
      <a
        :href="props.item.page"
        class="block shadow-orange-100 shadow-lg bg-gray-200 py-5 px-4 hover:bg-gray-300 rounded-lg"
        target="_blank"
      >
        <img
          src="@/assets/svg/link-solid.svg"
          alt="page"
          class="w-10 rotate-[165deg]"
        />
      </a>
      <a
        :href="props.item.github"
        class="block shadow-orange-100 shadow-lg bg-gray-200 py-4 px-4 hover:bg-gray-300 rounded-lg"
        target="_blank"
      >
        <img
          src="@/assets/svg/arrow-right-solid.svg"
          alt="github"
          class="w-10 rotate-[320deg]"
        />
      </a>
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

<style scoped>
.card:hover .img {
  width: 80%;
  height: 80%;
  transition: 300ms;
}
</style>
