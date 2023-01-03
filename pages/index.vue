<template>
  <main class="flex flex-col text-center w-full mt-20 justify-center items-center space-y-4">
    <h1 class="font-bold text-xl">Count</h1>
    <h3>{{ count }}</h3>
    <button
      class="text-green-600 border border-green-600 rounded-full justify-center px-5 w-fit hover:bg-green-600 hover:text-white"
      @click="addToCount">
      Increase Count
    </button>
  </main>
</template>

<script lang="ts">
import { ref, watchEffect, defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  setup() {
    const count = ref(0)

    function addToCount() {
      count.value++
    }

    watchEffect(() => {
      console.log(count.value);
    })

    return {
      count,
      addToCount
    }
  }
})
</script>