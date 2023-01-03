<template>
  <div class="flex flex-col min-h-screen bg-gray-100">
    <HeaderMenu class="px-8 md:px-20" />
    <Nuxt class="px-8 md:px-20" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeaderMenu from '@/components/HeaderMenu.vue'

export default defineComponent({
  name: 'Layout',
  components: {
    HeaderMenu
  }
})
</script>