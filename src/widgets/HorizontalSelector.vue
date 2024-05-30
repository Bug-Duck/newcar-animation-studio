<template>
  <div class="bg-[rgb(60,63,65)] w-full h-8 flex flex-row select-none">
    <HorizontalSelectorItem @click="bottomToolBox = 'animation'">Animations</HorizontalSelectorItem>
    <HorizontalSelectorItem @click="bottomToolBox = 'event'">Events</HorizontalSelectorItem>
  </div>
</template>

<script setup lang="ts">
import HorizontalSelectorItem from './HorizontalSelectorItem.vue'
import { inject } from 'vue'

const bottomToolBox = inject('bottomToolBox')
</script>