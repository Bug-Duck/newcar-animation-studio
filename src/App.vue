<script setup lang="ts">
import HorizontalSelector from './widgets/HorizontalSelector.vue'
import Selector from './widgets/Selector.vue'
import WidgetList from './widgets/WidgetList.vue'
import Editor from './widgets/Editor.vue'
import { provide, ref } from 'vue';

const bottomToolBox = ref<'animation' | 'event'>('animation')
const leftToolBox = ref<'attribute' | 'source'>('attribute')
provide('bottomToolBox', bottomToolBox)
provide('leftToolBox', leftToolBox)
</script>

<template>
  <div class="flex flex-grow flex-auto h-screen bg-gray-300">
    <div class="flex flex-col w-screen">
      <div class="w-full h-full bottom-6">
        <div class="float-left w-[30%] h-full bg-[rgb(60,63,65)] border border-[rgb(75,75,75)]">
          <Selector/>
          <div v-if="leftToolBox === 'attribute'">
            Attributes
          </div>
          <div v-else-if="leftToolBox === 'source'">
            Source
          </div>
        </div>
        <div class="float-left w-[70%] h-full bg-gray-400 border border-[rgb(75,75,75)] flex flex-col">
          <div class="w-full h-[60%] bg-[rgb(43,43,43)] border border-[rgb(75,75,75)]">
            <Editor/>
            <WidgetList/>
          </div>
          <div class="w-full h-[40%] bg-[rgb(43,43,43)] border border-[rgb(75,75,75)]">
            <HorizontalSelector/>
            <div v-if="bottomToolBox === 'animation'">
              Animation Editor
            </div>
            <div v-else-if="bottomToolBox === 'event'">
              event Editor
            </div>
          </div>
        </div>
      </div>
      <div class="w-full h-6 bottom-0">
        <div class="h-6 bg-[rgb(60,63,65)] w-full">www</div>
      </div>
    </div>
  </div>
</template>