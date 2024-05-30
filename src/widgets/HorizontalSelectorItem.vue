<template>
  <div class="text-white text-center h-full px-5 pt-1 text-base hover:bg-[rgb(75,75,75)]" :class="{
    'float-left': props.position === 'left',
    'float-right': props.position === 'right'
  }">
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  position: String
})
</script>