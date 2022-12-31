<template>
    <button @click="buttonHandler">{{ props.text }}</button>
</template>

<script setup lang="ts">


// --------------------------------------------------------------
// Data, methods and functions
// ---------------------------------------------------------------

const props = defineProps([
    'text'
])

const emit = defineEmits([
    'buttonHandler'
])

function buttonHandler(e: any) {
    e.preventDefault()
    console.log("button");
    emit("buttonHandler");
}


</script>

<style>

button {
    min-height: 6em;
    width: 45%;
    border-radius: 15px;
    cursor: pointer;
    margin: 15px 0;
    margin-bottom: 0;
    font-weight: bold;
}

</style>