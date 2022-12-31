<template>
    <section class="content" >
        <FormHeader />
        <AddNewItemForm @formSubmit="(newItem) =>handleSubmit(newItem)"/>
        <!-- <GlobalSettingsForm /> -->

    </section>
</template>

<script setup lang="ts">
import FormHeader from './FormHeader.vue'
import AddNewItemForm from './AddNewItemForm.vue';
import GlobalSettingsForm from './GlobalSettingsForm.vue'

const emit = defineEmits([
    'formSubmit'
])

function handleSubmit(newItem) {
    // e.preventDefault()
    console.log("topLevel");
    console.log(newItem)
    emit("formAction", newItem);
}

</script>



<style scoped>

section {
  background: #fff;
  filter: var(--drop-shadow);
  margin: var(--mobile-gutters);
  border-radius: var(--border-containers);
  padding-top: 1em;
  overflow: hidden;
  width: 100%;
  /* height: 100%; */
}

@media screen and (min-width: 1200px) {
    section {
        width: 30%;
        margin-top: 20px;
    }
}

</style>