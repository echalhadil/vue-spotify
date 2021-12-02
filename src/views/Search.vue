<template>
  <div class="w-full pb-44 text-white px-8 h-screen overflow-y-auto scrollbar-thin">
    <div></div>
    <div class="pt-4">
      <div class="font-bold text-2xl">Your favorite genres</div>
      <div class="capitalize py-4 flex scrollbar-thin gap-4 select-none overflow-x-auto">
        <favorite-genre
          v-for="(genre, index) in genres"
          :key="index"
          :name="genre"
          :src="getImageLink()"
        />
      </div>
    </div>

    <div class="pt-4">
      <div class="font-bold text-2xl">Show all</div>
      <div class="grid sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-5 gap-x-5 gap-y-4 pt-3">
        <genre
          v-for="(genre, index) in genres"
          :key="index"
          :name="genre"
          :src="getImageLink()"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Genre from "../components/Genre";
import FavoriteGenre from "../components/FavoriteGenre";

export default {
  name: "Search",
  components: { Genre, FavoriteGenre },
  data() {
    return {
      genres: this.$store.getters.getGenres,
    };
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
