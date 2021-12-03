<template>
  <div class="w-full pb-44 h-screen overflow-y-auto scrollbar-thin">
    <div class="px-8">
      <div>Playlists</div>
      <div class="grid md:grid-cols-2 xl:grid-cols-5 w-full gap-4">
        <div
          class="bg-gradient-to-br rounded-md p-4 grid grid-rows-3 text-white col-span-2 from-purple-600 to-purple-300"
        >
          <div class="invisible md:visible"></div>
          <div class="font-semibold">
            <span>
              <span>inkonnu </span>
              <span class="text-gray-200">Tab3ini V2</span>
            </span>
            <span> • </span>

            <span>
              <span>inkonnu </span>
              <span class="text-gray-200">Tab3ini V2</span>
            </span>
            <span> • </span>
            <span>
              <span>inkonnu </span>
              <span class="text-gray-200">Tab3ini V2</span>
            </span>
            <span>
              <span>inkonnu </span>
              <span class="text-gray-200">Tab3ini V2</span>
            </span>
            <span> • </span>
            <span>
              <span>inkonnu </span>
              <span class="text-gray-200">Tab3ini V2</span>
            </span>
          </div>
          <div class="">
            <div class="text-3xl font-bold" as="div">Liked tracks</div>
            <div>
              <div class="font-semibold">48 Titres likés</div>
            </div>
          </div>
        </div>
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
        <song :src="getImageLink()" />
      </div>
    </div>
    <div></div>
  </div>
</template>

<script>
import Song from "../components/Song";
export default {
  components: {
    Song,
  },

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
