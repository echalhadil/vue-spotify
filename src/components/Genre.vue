<template>
  <div
    :class="
      'py-3 cursor-pointer hover:opacity-95 px-4 space-y-10 rounded-md overflow-hidden ' +
      $store.getters.getRandomBgColor
    "
  >
    <div class="font-bold capitalize text-xl">
      <p>{{ name }}</p>
    </div>
    <picture class="bg-gray-800 h-24 w-24 transform rotate-45 -mr-10 float-right">
      <source :srcset="src" type="image/jpg" />
      <img
        class="shadow-md"
        :src="src"
        aria-hidden="false"
        draggable="false"
        loading="lazy"
        alt=""
      />
    </picture>
  </div>
</template>

<script>
export default {
  name: "genre",
  props: {
    name: String,
    src: String,
  },
};
</script>
