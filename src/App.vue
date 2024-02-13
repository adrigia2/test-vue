<script setup>
import {
  NButton, NFlex, NGradientText
} from 'naive-ui'
import { ref } from 'vue'

let width = ref(100)
let height = ref(100)

const handleNo = () => {
  // scale up the button si
  width.value *= 3
  height.value *= 3
}


const handleYes = () => {
  alert('Ci vediamo domani Ari mia stupenda')
}


</script>

<template>
  <div class="main">
    <n-flex vertical>
      <n-gradient-text type="danger" :size="72">
        Ari mia stupenda, vuoi passare San Valentino con me?
      </n-gradient-text>
      <n-flex class="center">
        <n-button :style="{ width: `${width}px`, height: `${height}px` }" type="primary" @click="handleYes">Si</n-button>
        <n-button @click="handleNo">No</n-button>
      </n-flex>
    </n-flex>
  </div>
</template>

<style>
.main {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.center {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>

