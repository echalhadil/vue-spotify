<template>
  <div
    class="flex p-4 text-white absolute bottom-0 justify-between bg-gray-800 border-gray-700 shadow-md border-t w-full"
  >
    <div class="flex space-x-4 items-center">
      <div class="w-14 h-14 bg-white"></div>
      <div>
        <p class="text-sm font-semibold">Talan</p>
        <p class="text-xs text-gray-400">Smallx</p>
      </div>
      <div class="flex pl-3 items-center space-x-3">
        <HeartIcon class="text-sm h-5 w-5 text-gray-500" />
        <AnnotationIcon class="text-sm h-5 w-5 text-gray-500" />
      </div>
    </div>
    <div class="flex-grow px-12">
      <div class="flex pl-3 justify-center items-center space-x-3">
        <HeartIcon class="h-5 w-5 text-gray-500" />
        <ChevronLeftIcon class="h-5 w-5 text-gray-500" />
        <PauseIcon class="h-11 w-11 text-white" />
        <ChevronRightIcon class="h-5 w-5 text-gray-500" />
        <RefreshIcon class="h-5 w-5 text-gray-500" />
      </div>
      <div class="flex pl-3 items-center text-xs text-gray-400 space-x-3">
        <div>0:00</div>
        <div class="w-full bg-white h-1 rounded-full"></div>

        <div>1:00</div>
      </div>
    </div>
    <div class="flex space-x-4 items-center">
      <div class="flex pl-3 items-center text-gray-500 space-x-3">
        <MicrophoneIcon class="h-5 w-5" />
        <AnnotationIcon class="h-5 w-5" />
        <DesktopComputerIcon class="h-5 w-5" />
        <VolumeUpIcon class="h-5 w-5" />
        <div class="h-1 rounded-full w-24 bg-white"></div>
      </div>
    </div>
  </div>
</template>
<script>
import {
  HeartIcon,
  MicrophoneIcon,
  VolumeUpIcon,
  AnnotationIcon,
  ChevronLeftIcon,
  ChevronRightIcon,
  RefreshIcon,
  DesktopComputerIcon,
} from "@heroicons/vue/outline";
import { PauseIcon } from "@heroicons/vue/solid";
export default {
  name: "Player",
  components: {
    HeartIcon,
    VolumeUpIcon,
    MicrophoneIcon,
    AnnotationIcon,
    PauseIcon,
    ChevronLeftIcon,
    ChevronRightIcon,
    RefreshIcon,
    DesktopComputerIcon,
  },
};
</script>
