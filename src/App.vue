<script setup lang="ts">
import LootboxArea from './components/lootbox/LootboxArea.vue';
import Navigation from './components/Navigation.vue';
import FormArea from './components/form/FormArea.vue';

// components: { LootboxArea, Navigation }

</script>

<template>
  <div class="main-container">
    <header>
      <Navigation />
    </header>

    <main>
      <LootboxArea />
      <FormArea />
    </main>
  </div>
</template>

<style scoped>
  .main-container {
    width: 96%;
    margin: auto;
  }

  @media screen and (min-width: 1200px) {
    main {
      display: flex;
      flex-direction: row;
      gap: 25px
    }
  }
</style>
