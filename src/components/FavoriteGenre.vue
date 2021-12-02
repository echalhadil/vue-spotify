<template>
  <div
    :class="
      'pl-4 pt-4 flex-none rounded-md overflow-hidden cursor-pointer hover:opacity-95 scrollbar-none w-2/5 ' +
      $store.getters.getRandomBgColor
    "
  >
    <p class="text-5xl font-bold">{{ name }}</p>

    <picture class="bg-gray-600 h-32 w-32 float-right -mr-8 rotate-45 transform">
      <source :srcset="src" type="image/jpg" />
      <img class="shadow-md" :src="src" loading="lazy" alt="" />
    </picture>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    src: String,
  },
};
</script>
