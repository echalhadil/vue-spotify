<template>
  <div class="h-screen overflow-hidden bg-gray-900">
    <main class="flex">
      <Sidebar />
      <router-view v-slot="{ Component }">
        <transition
          mode="out-in"
          duration="200"
          enter-class="opacity-0  translate-y-8 "
          leave-to-class=" opacity-0 translate-y-8 "
          enter-active-class="transition-all  ease-in-out "
          leave-active-class="transition-all   ease-in-out  "
        >
          <component :is="Component" />
        </transition>
      </router-view>
    </main>
    <Player />
  </div>
</template>

<script>
import Sidebar from "./components/Sidebar";
import Player from "./components/Player";
export default {
  name: "App",
  components: {
    Sidebar,
    Player,
  },
};
</script>
