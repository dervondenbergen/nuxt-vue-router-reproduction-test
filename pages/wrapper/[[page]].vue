<script setup lang="ts">
definePageMeta({
  name: 'wrapper-sub',
});

const route = useRoute();
</script>

<template>
  <div>
    <h1>Wrapper Sub Page</h1>
    <p>Current route: {{ route.params }}</p>
  </div>
</template>
