<template>
    <form class="content" >
        <div class="form-control">
            <label for="item-name">Item Name</label>
            <input v-model="itemNameText" class="text" name="item-name" type="text">
        </div>
        <div class="form-control">
            <label for="percent-change">Percent Chance</label>
            <input v-model="percentChance" class="text" name="item-name" type="number">
        </div>
        <div class="form-control">
            <label for="item-description">Item Description</label>
            <input v-model="itemDescriptionText" class="text-area text" name="item-description" type="text">
        </div>
        
        <div class="form-control">
            <label for="item-image">Upload Image</label>
            <input name="item-image" type="file">
        </div>

        <AppButton @buttonHandler="handleForm" type="submit" text="Save" />
    </form>
</template>


<script lang="ts" setup>
import AppButton from '../blocks/AppButton.vue'
import { ref } from 'vue'

let itemNameText = ref<string>('');
let itemDescriptionText = ref<string>('');
let percentChance = ref<number>();
let imgPath = "https://via.placeholder.com/100"
let imgAlt = itemDescriptionText;

let newItem = { id: (Math.floor(Math.random()) * 1000), title: itemNameText, itemDescription: itemDescriptionText, imgSrc: imgPath, imgAlt: itemDescriptionText, percentChance: percentChance };
// let newItem = {id: 100, title: 'titleTxt', itemDescription: "item description text", imgSrc: "https://via.placeholder.com/100", imgAlt: "something alty", percentChance: 50}

let clearForm = () => {
    alert('remember to clear form')
}


// let handleForm = () => {
//     alert('worked!')
// }

const emit = defineEmits([
    'formSubmit'
])

function handleForm(e: any) {
    // e.preventDefault()
    console.log("form");
    // console.log(newItem)
    emit("formSubmit", newItem);
    clearForm();
}


</script>
