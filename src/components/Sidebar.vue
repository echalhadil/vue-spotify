<template>
  <div class="bg-black md:w-max invisible md:visible w-0 text-gray-200 h-screen">
    <div class="flex space-x-1 p-6 pr-20">
      <img src="../assets/logo.png" class="w-9 my-auto h-9" alt srcset />
      <h1 class="my-auto font-bold text-2xl font-sans text-white">Spotify</h1>
    </div>
    <div class="px-2">
      <div class="space-y-1">
        <custom-router-link to="/" label="Home">
          <HomeIcon class="h-6 w-6 text-gray-400" />
        </custom-router-link>
        <custom-router-link to="/search" label="Search">
          <SearchIcon class="h-6 w-6 text-gray-400" />
        </custom-router-link>
        <custom-router-link to="/playlists" label="Library">
          <BookOpenIcon class="h-6 w-6 text-gray-400" />
        </custom-router-link>
      </div>

      <div class="pt-6">
        <div
          class="flex space-x-3 px-4 py-2 cursor-pointer rounded font-semibold text-sm hover:bg-gray-700 hover:text-gray-100"
        >
          <PlusIcon class="h-6 w-6 text-gray-400" />

          <div class="my-auto">Create playlist</div>
        </div>
        <div
          class="flex space-x-3 px-4 py-2 cursor-pointer rounded font-semibold text-sm hover:bg-gray-700 hover:text-gray-100"
        >
          <HeartIcon class="h-6 w-6 text-gray-400" />
          <div class="my-auto">Your likes</div>
        </div>
        <div
          class="flex space-x-3 px-4 py-2 cursor-pointer rounded font-semibold text-sm hover:bg-gray-700 hover:text-gray-100"
        >
          <BookOpenIcon class="h-6 w-6 text-gray-400" />
          <div class="my-auto">Your episodes</div>
        </div>
        <hr class="mx-4 mt-2 border-opacity-25 pb-6 border-gray-300" />
      </div>

      <div
        class="overflow-y-auto scrollbar-thin scrollbar-thumb-gray-900 scrollbar-track-black max-h-48 text-gray-400"
      >
        <div
          v-for="(playlist, index) in playlists"
          :key="index"
          class="flex space-x-3 cursor-pointer select-none capitalize px-4 py-2 font-semibold text-sm hover:text-white"
        >
          <p class="my-auto truncate">{{ playlist }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import {
  HeartIcon,
  HomeIcon,
  SearchIcon,
  BookOpenIcon,
  PlusIcon,
} from "@heroicons/vue/outline";
import CustomRouterLink from "./CustomRouterLink";
import { mapState } from "vuex";

export default {
  name: "Sidebar",
  components: {
    HeartIcon,
    HomeIcon,
    SearchIcon,
    BookOpenIcon,
    PlusIcon,
    CustomRouterLink,
  },
  computed: {
    ...mapState(["playlists"]),
  },
};
</script>
