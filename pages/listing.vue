<template>
  <main class="flex flex-col items-center mt-20">
    <h1 class="font-bold text-xl">Listing</h1>
    <ul class="flex flex-col space-y-2 mt-2">
      <li v-for="friend in listOfFriends" :key="friend" class="hover:bg-gray-200 rounded-full px-3 cursor-pointer"
        @click="alertUnit">
        {{ friend }}
      </li>
    </ul>
    <p class="mt-2 text-sm text-gray-500 italic">Click on a friend!</p>
  </main>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue';


export default defineComponent({
  name: 'ListingPage',
  setup() {
    const state = reactive({
      listOfFriends: [
        'Sarah likes all tacos',
        'Brian Holt likes whiskey more than tacos',
        'Shirley Wu likes tacos as much as Wonder Woman'
      ]
    })

    function alertUnit(evt: Event) {
      alert((evt.target as HTMLInputElement).textContent?.trim())
    }

    return {
      ...toRefs(state),
      alertUnit
    }
  }
})
</script>