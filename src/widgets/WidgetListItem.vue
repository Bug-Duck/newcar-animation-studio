<template>
  <ul>
    <li class="text-[14px] pl-4">
      <div class="hover:bg-[rgb(75,75,75)] w-full">{{ tree.name }}</div>
      <ul class="hover:bg-none">
        <li v-for="child in tree.children">
          <WidgetListItem :tree="child" />
        </li>
      </ul>
    </li>
  </ul>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
import type { Widget } from 'newcar'

interface WidgetTree {
  widget: Widget
  children?: WidgetTree[]
  name: string
}

const { tree } = defineProps<{
  tree: WidgetTree
}>(); 
</script>