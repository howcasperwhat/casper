<script setup lang='ts'>
import { studyProcesses, studyTypes } from '../stores/data'
import Routes from './Routes.vue'
import Process from './Process.vue'

defineProps<{ active: number }>()
</script>

<template>
  <div grid="~ flow-row sm:flow-col gap-6" class="slide-content">
    <Routes :active="active" :types="studyTypes" class="route" />
    <Process :processes="studyProcesses[active]" class="slide-content" />
  </div>
</template>
