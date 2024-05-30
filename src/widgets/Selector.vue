<template>
  <div class="float-left h-full w-12 bg-[rgb(60,63,65)] border border-[rgb(75,75,75)] select-none">
    <SelectorItem @click="leftToolBox = 'attribute'">A</SelectorItem>
    <SelectorItem @click="leftToolBox = 'source'">S</SelectorItem>
  </div>
</template>

<script setup lang="ts">
import SelectorItem from './SelectorItem.vue'
import { inject } from 'vue'

const leftToolBox = inject('leftToolBox')
</script>