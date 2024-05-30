<script setup lang="ts">
import HorizontalSelector from './widgets/HorizontalSelector.vue'
import Selector from './widgets/Selector.vue'
</script>

<template>
  <div class="flex flex-grow flex-auto h-screen bg-gray-300">
    <div class="flex flex-col w-screen">
      <div class="w-full h-full bottom-6">
        <div class="float-left w-[30%] h-full bg-[rgb(60,63,65)] border border-[rgb(75,75,75)]">
          <Selector/>
        </div>
        <div class="float-left w-[70%] h-full bg-gray-400 border border-[rgb(75,75,75)] flex flex-col">
          <div class="w-full h-[60%] bg-[rgb(43,43,43)] border border-[rgb(75,75,75)]"></div>
          <div class="w-full h-[40%] bg-[rgb(43,43,43)] border border-[rgb(75,75,75)]">
            <HorizontalSelector/>
          </div>
        </div>
      </div>
      <div class="w-full h-6 bottom-0">
        <div class="h-6 bg-[rgb(60,63,65)] w-full">www</div>
      </div>
    </div>
  </div>
</template>