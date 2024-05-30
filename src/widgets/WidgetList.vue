<template>
  <div class="h-full w-[20%] float-left bg-[rgb(60,63,65)] flex flex-col text-white">
    <WidgetListItem :tree="{
      widget: new Widget(),
      children: [
        {
          widget: new Widget(),
          children: [],
          name: 'root'
        }
      ],
      name: 'root'
    }"/>
  </div>
</template>

<script setup lang="ts">
import { Widget } from 'newcar';
import WidgetListItem from './WidgetListItem.vue'
</script>