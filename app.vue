<template>
  <div class="app">
    <header>Hello Header</header>
    <nav>
      <ul>
        <li><NuxtLink :to="{ name: 'home' }">Index</NuxtLink></li>
        <li><NuxtLink :to="{ name: 'wrapper' }">Wrapper</NuxtLink></li>
      </ul>
    </nav>
    <NuxtPage />
  </div>
</template>
