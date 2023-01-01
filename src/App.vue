<template>
  <div class="main-container">
    <header>
      <Navigation />
    </header>

    <main>
      <LootboxArea :lootboxItems="lootboxItems" @close-button-handle="(id) => closeButtonHandle(id)" />
      <FormArea @formAction="(newItem) => formAction(newItem)" />

    </main>
  </div>
</template>

<script setup lang="ts">

// --------------------------------------------------------------
// Imports
// ---------------------------------------------------------------

// Components 
import LootboxArea from './components/lootbox/LootboxArea.vue';
import Navigation from './components/Navigation.vue';
import FormArea from './components/form/FormArea.vue';

// Modules 
import { ref } from 'vue'

// Types 
import type LootboxItem from './components/types/LootboxItem'

// --------------------------------------------------------------
// Data, methods and functions
// ---------------------------------------------------------------

// Data

let lootboxItems = ref<LootboxItem[]>([
  {id: 1, title: 'titleTxt', itemDescription: "item description text", imgSrc: "https://via.placeholder.com/100", imgAlt: "something alty", percentChance: 50},
  {id: 2, title: 'titleTxt', itemDescription: "item description text", imgSrc: "https://via.placeholder.com/100", imgAlt: "something alty", percentChance: 50},
  {id: 3, title: 'titleTxt', itemDescription: "item description text", imgSrc: "https://via.placeholder.com/100", imgAlt: "something alty", percentChance: 50}
])

// Methods

const addLootboxItem = (id: number, title: string, itemdescription: string, imgSrc: string, imgAlt: string, percentChance: number) => {
  lootboxItems.value = [...lootboxItems.value, {id, title, itemdescription, imgSrc, imgAlt, percentChance} as unknown as LootboxItem]
}

const removeLootboxItem = ( id: number ) => {
  lootboxItems.value = [...lootboxItems.value].filter( item => item.id != id)
}

const formAction = (newItem) => {
  console.log("yep")
  // console.log(newItem)
  addLootboxItem(newItem.id, newItem.title, newItem.description, newItem.imgSrc, newItem.imgAlt, newItem.percentChance);
}

let closeButtonHandle = (id) => {
  removeLootboxItem(id);
}

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
