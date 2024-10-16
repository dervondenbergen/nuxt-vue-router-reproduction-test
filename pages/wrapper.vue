<script setup lang="ts">
definePageMeta({
  name: 'wrapper',
});

const subPages = ['A', 'B', 'C', 'D', 'E'];

const route = useRoute();

const page = computed(() => {
  return subPages.find((page) => page === (route.params.page as string));
});

watchEffect(() => {
  if (!page.value) {
    return navigateTo(
      { name: 'wrapper-sub', params: { page: subPages[0] } },
      { replace: true }
    );
  }
});
</script>

<template>
  <div>
    <h1>Wrapper Page</h1>
    <p>
      Current route: via route params {{ route.params }} and via computed
      {{ page }}
    </p>
    <ul>
      <li v-for="page in subPages" :key="page">
        <NuxtLink :to="{ name: 'wrapper-sub', params: { page: page } }">{{
          page
        }}</NuxtLink>
      </li>
    </ul>
  </div>
</template>
