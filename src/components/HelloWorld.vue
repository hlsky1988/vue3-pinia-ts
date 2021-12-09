<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <h1>{{ homeStore.num }}</h1>
    <!-- <h1>{{ homeStore.doubleNum }}</h1> -->
    {{ homeStore.text }}
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
import { useHomeStore } from "@/stores/home";

const props = defineProps({
  msg: {
    type: String,
    required: true,
  },
})

const homeStore = useHomeStore()

setTimeout(() => {
  console.log(homeStore.text);
  homeStore.text = 'hello pinia'
  homeStore.numAdd()
}, 5000);
</script>

<style scoped lang="less"></style>
