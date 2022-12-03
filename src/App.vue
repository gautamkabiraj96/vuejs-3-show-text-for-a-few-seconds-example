<script setup>
import { ref } from 'vue'

const textVisible = ref(false)

const showText = () => {
  textVisible.value = true

  setTimeout(() => {
    textVisible.value = false
  }, 3000)
}

</script>

<template>
<div>
    <button @click="showText">
      Sign up
    </button>
    <h1 v-if="textVisible">
      Thanks for signing up! 
    </h1>
</div>
</template>