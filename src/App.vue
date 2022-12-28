<script setup lang="ts">
import LootboxArea from './components/LootboxArea.vue';
import Navigation from './components/Navigation.vue';

// components: { LootboxArea, Navigation }

</script>

<template>
  <div class="main-container">
    <header>
      <Navigation />
    </header>

    <main>
      <lootbox-area />
    </main>
  </div>
</template>

<style scoped>
  .main-container {
    width: 96%;
    margin: auto;
  }
</style>
