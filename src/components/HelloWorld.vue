<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
const props = defineProps({
  msg: {
    type: String,
    required: true,
  },
})
</script>

<style scoped lang="less"></style>
