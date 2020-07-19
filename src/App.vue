<template>
  <div>
    <TeleportText />
    <img alt="Vue logo" src="./assets/logo.png" />
    <Suspense>
      <template #default>
        <AsyncSuspens />
      </template>
      <template #fallback>
        Loading...
      </template>
    </Suspense>
  </div>
</template>

<script lang='ts'>
import { ref ,defineComponent } from 'vue'
import TeleportText from './components/TeleportText.vue'
import AsyncSuspens from './components/AsyncSuspens.vue'

export default defineComponent ({
  name: 'App',
  components: {
    TeleportText,
    AsyncSuspens
  }, 
  setup() {}
})
</script>
