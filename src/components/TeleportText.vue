<template>
  <div>
    <button @click="toggle">Button</button>
    <!--teleport先は<div id="app">外でなければいけない-->
    <teleport to="#target">
      <div v-if="isBool">
        <p>Teleport</p>
        <button @click="toggle">Button</button>
      </div>
    </teleport>
  </div>
</template>

<script lang='ts'>
import { defineComponent, ref } from 'vue'
export default defineComponent ({
  setup() {
    const isBool = ref(false)
    const toggle = () => {
      isBool.value = !isBool.value
    }

    return {
      isBool,
      toggle
    }
  }
})
</script>
