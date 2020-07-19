<template>
  <div>
    <div id="target"></div>
    <button @click="toggle">Button</button>
    <!--err-->
    <Teleport to="#target">
      <div v-if="isBool">
        <p>Teleport</p>
        <button @click="toggle">Button</button>
      </div>
    </Teleport>
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
