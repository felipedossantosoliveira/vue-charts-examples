<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
<header class="flex items-center justify-between m-10">
  <div class="text-3xl font-bold">
    <RouterLink to="/">Vue 3 Charts Examples</RouterLink>
  </div>
</header>
<div class="m-10">
  <RouterView />
</div>
</template>