<script setup>
import { ref } from "vue";

const keyword = ref("");
</script>
<template>
  <form class="space-x-2">
    <input
      type="search"
      v-model="keyword"
      class="w-[60vw] rounded-md focus:outline-none focus-within:ring-zinc-900 focus:border-zinc-900"
      placeholder="Type book name, author..."
    />
    <button
      @click.prevent="$emit('search', { keyword })"
      class="py-2 px-4 rounded-md bg-zinc-900 text-zinc-100 hover:bg-zinc-900/90"
    >
      Search
    </button>
  </form>
</template>
