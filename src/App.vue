<template>
  <div class="main-container">
    <header>
      <Navigation />
    </header>

    <main>
      <LootboxArea :lootboxItems="lootboxItems" />
      <FormArea />
      <!-- <p>{{ lootboxItems }}</p> -->
      <!-- <p>{{  lootboxItems }}</p> -->
    </main>
  </div>
</template>

<script setup lang="ts">
import LootboxArea from './components/lootbox/LootboxArea.vue';
import Navigation from './components/Navigation.vue';
import FormArea from './components/form/FormArea.vue';

import { reactive } from '@vue/reactivity';
import { ref, toRefs } from 'vue'
import type LootboxItem from './components/types/LootboxItem'

const lootboxItems = ref([
  {title: 'titleTxt'}
])

</script>



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
