<template>
  <div
    class="bg-gray-700 p-3 bg-opacity-50 shadow rounded cursor-pointer hover:bg-gray-600 transition duration-500"
  >
    <picture class="min-h-40 bg-green-600">
      <source :srcset="src" type="image/jpg" />
      <img
        class="shadow-sm w-full"
        :src="src"
        aria-hidden="false"
        draggable="false"
        loading="lazy"
        alt=""
      />
    </picture>

    <div class="pt-5 py-2">
      <div class="font-semibold">Liked Songs</div>
      <div class="uppercase text-xs pt-1 text-gray-300">25 nov . 20 MIN</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Song",
  props: {
    src: String,
  },
};
</script>
