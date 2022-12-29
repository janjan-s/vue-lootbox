<template>
    <nav class="header">
        <ul>
            <li class="selected"><h2>Add new item</h2></li>
            <li><h2>Global Settings</h2></li>
        </ul>
    </nav>
</template>


<script lang="ts">
import { defineComponent } from "@vue/runtime-core";

export default defineComponent({
    name: 'FormHeader'
})

</script>


<style scoped>

ul {
    list-style-type: none;
    display: flex;
    padding: 0;
    text-align: center;
}

li {
    flex: 1 1 50%;
    background: #706993;
    /* cursor: pointer; */
}

li:not(.selected) {
    cursor: pointer;
}

li.selected {
    background: blue;
    cursor: default;
}

</style>