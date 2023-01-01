<template>
    <form class="content" >
        <div class="form-control">
            <label for="item-name">Item Name</label>
            <input required v-model="itemNameText" class="text" name="item-name" type="text">
        </div>
        <div class="form-control">
            <label for="percent-change">Percent Chance</label>
            <input required v-model="percentChance" class="text" name="item-name" type="number">
        </div>
        <div class="form-control">
            <label for="item-description">Item Description</label>
            <input required v-model="itemDescriptionText" class="text-area text" name="item-description" type="text">
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

const formInitialState =  {
    itemName: '',
    percentChance: 0,
    itemDescriptionText: '',
}

let itemNameText = ref<string>('');
let itemDescriptionText = ref<string>('');
let percentChance = ref<number>();
let imgPath = "https://via.placeholder.com/100"
let imgAlt = itemDescriptionText;

// let newItem = {id: 100, title: 'titleTxt', itemDescription: "item description text", imgSrc: "https://via.placeholder.com/100", imgAlt: "something alty", percentChance: 50}

let clearForm = () => {
    // alert('remember to clear form')
    itemNameText.value = '';
    itemDescriptionText.value = '';
    percentChance.value = 0;
    // imgPath.value = "https://via.placeholder.com/100"
    imgAlt.value = '';
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
    let newItem = { id: (Math.floor(Math.random() * 1000) ), title: itemNameText.value, itemDescription: itemDescriptionText.value, imgSrc: imgPath, imgAlt: itemDescriptionText.value, percentChance: percentChance.value };

    emit("formSubmit", newItem);
    clearForm();
}


</script>
