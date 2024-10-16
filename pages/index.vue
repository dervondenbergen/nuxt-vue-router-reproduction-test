<script setup lang="ts">
definePageMeta({
  name: 'home',
});

const route = useRoute();
</script>

<template>
  <div>
    <h1>Index Page</h1>
    <p>Current route: {{ route.path }}</p>
    <p>Lorem Ipsum …</p>
  </div>
</template>
