<template>
    <button>CLICK</button>
</template>

<script lang="ts">
import { defineComponent } from "@vue/runtime-core";


export default defineComponent({
    name: 'AppButton',
})

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