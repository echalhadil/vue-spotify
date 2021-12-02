<template>
  <div class="w-full pb-44 h-screen overflow-y-auto scrollbar-thin">
    <div
      :class="
        'transition duration-500 text-white bg-gradient-to-b  to-gray-900 ' +
      $store.getters.getRandomBgColor
      "
    >
      <div class="flex justify-between items-center relative px-8 py-3">
        <div class="mr-auto flex space-x-4">
          <ArrowLeftIcon
            class="cursor-pointer h-8 p-2 w-8 text-gray-400 bg-gray-900 rounded-full"
          />
          <ArrowRightIcon
            class="cursor-pointer h-8 p-2 w-8 text-gray-400 bg-gray-900 rounded-full"
          />
        </div>
        <div class="ml-auto flex items-center space-x-4">
          <button
            class="uppercase font-semibold border rounded-full px-6 bg-gray-900 py-1"
          >
            Subscribe
          </button>
          <div
            class="font-semibold flex items-center justify-between space-x-2 p-0.5 rounded-full bg-gray-900"
          >
            <UserIcon class="h-8 p-2 w-8 rounded-full bg-gray-500" />
            <div>echalh-adil</div>
            <ArrowDownIcon class="h-8 p-2 w-8" />
          </div>
        </div>
      </div>

      <div class="p-8">
        <div class="font-bold text-4xl">Hello</div>
        <div class="pt-5 grid sm:grid-cols-2 xl:grid-cols-3 gap-y-4 gap-x-6">
          <div
            class="bg-gray-700 bg-opacity-50 shadow items-center grid grid-cols-4 space-x-3 rounded"
          >
            <div
              class="bg-gradient-to-br h-full col-span-1 items-center rounded-l from-indigo-700 to-white"
            >
              <HeartIcon class="h-8 w-8 relative text-white" />
            </div>
            <div class="col-span-3 font-semibold">Liked Songs</div>
          </div>
          <div
            class="bg-gray-700 bg-opacity-50 shadow grid grid-cols-4 items-center space-x-3 rounded"
          >
            <div class="bg-gradient-to-br col-span-1 rounded-l from-pink-700 to-white">
              <img :src="getImageLink()" class="rounded-sm h-full w-full" alt srcset />
            </div>
            <div class="col-span-3 font-semibold">Liked Songs</div>
          </div>
          <div
            class="bg-gray-700 bg-opacity-50 shadow grid grid-cols-4 items-center space-x-3 rounded"
          >
            <div class="bg-gradient-to-br col-span-1 rounded-l from-pink-700 to-white">
              <img :src="getImageLink()" class="rounded-sm h-full w-full" alt srcset />
            </div>
            <div class="col-span-3 font-semibold">Liked Songs</div>
          </div>
          <div
            class="bg-gray-700 bg-opacity-50 shadow grid grid-cols-4 items-center space-x-3 rounded"
          >
            <div class="bg-gradient-to-br col-span-1 rounded-l from-pink-700 to-white">
              <img :src="getImageLink()" class="rounded-sm h-full w-full" alt srcset />
            </div>
            <div class="col-span-3 font-semibold">Liked Songs</div>
          </div>
          <div
            class="bg-gray-700 bg-opacity-50 shadow grid grid-cols-4 items-center space-x-3 rounded"
          >
            <div class="bg-gradient-to-br col-span-1 rounded-l from-pink-700 to-white">
              <img :src="getImageLink()" class="rounded-sm h-full w-full" alt srcset />
            </div>
            <div class="col-span-3 font-semibold">Liked Songs</div>
          </div>
          <div
            class="bg-gray-700 bg-opacity-50 shadow grid grid-cols-4 items-center space-x-3 rounded"
          >
            <div class="bg-gradient-to-br col-span-1 rounded-l from-pink-700 to-white">
              <img :src="getImageLink()" class="rounded-sm h-full w-full" alt srcset />
            </div>
            <div class="col-span-3 font-semibold">Liked Songs</div>
          </div>
        </div>
      </div>
    </div>
    <div class="px-8 py-3 text-white">
      <div class="font-bold text-2xl">Episodes for ou</div>
      <div class="pt-5 grid sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-5 gap-y-4 gap-x-6">
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
      </div>
    </div>

    <div class="px-8 py-3 text-white">
      <div class="font-bold text-2xl">You might like</div>
      <div class="pt-5 grid sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-5 gap-y-4 gap-x-6">
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
      </div>
    </div>
  </div>
</template>

<script>
import {
  ArrowRightIcon,
  ArrowLeftIcon,
  ArrowDownIcon,
  UserIcon,
  HeartIcon,
} from "@heroicons/vue/outline";
import Song from "../components/Song";
export default {
  name: "Home",
  components: { Song, ArrowRightIcon, ArrowLeftIcon, ArrowDownIcon, UserIcon, HeartIcon },
  methods: {
    getImageLink() {
      let randomInt = 0;
      do {
        randomInt = parseInt(Math.random() * 1000);
      } while (randomInt < 300);
      return "https://picsum.photos/" + randomInt;
    },
  },

};
</script>
