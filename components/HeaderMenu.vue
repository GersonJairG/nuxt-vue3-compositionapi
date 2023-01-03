<template>
  <nav class="flex w-full bg-slate-800 text-white h-14 items-center">
    <ul class="flex space-x-5">
      <li>
        <nuxt-link exact to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/listing">Listing</nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HeaderMenu',
  props: {
    classes: {
      type: String,
      default: ''
    }
  }
})
</script>