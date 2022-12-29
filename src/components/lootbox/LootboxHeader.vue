<template>
    
    <!-- <div class="lootbox-area"> -->
      <div class="information content">
    
        <div class="column one">
          <img src="https://via.placeholder.com/275" alt="">
        </div>

        <div class="column two">
          <h2>Title</h2>
          <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laudantium reprehenderit magnam vitae distinctio ipsum fuga excepturi, rem placeat laborum illum molestias cumque assumenda aliquam hic iste voluptatibus incidunt nemo. Eligendi?</p>
        </div>

        <div class="column three">
          <div class="bubble">
            <h3>7</h3>
            <span>Items</span>
          </div>
          <div class="bubble">
            <h3>5</h3>
            <span>Prizes</span>
          </div>
        </div>

      </div>
    <!-- </div> -->

</template>




<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LootboxHeader',
})
</script>

<style scoped>

/* .lootbox-area {
  background: #fff;
  filter: var(--drop-shadow);
  margin: var(--mobile-gutters);
  border-radius: var(--border-containers);
} */

.information {
  display: flex;
  flex-direction: row;
  gap: 10px;
}

.column {
  flex: 1 1 25%;
}

.column.one img {
  width: 135px;
  height: 135px
}

.column.two {
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 5;
  /* autoprefixer: ignore next */
  -webkit-box-orient: vertical; 

  overflow: hidden;
  flex: 40%;
  height: 145px;
}

.column.two p {
  color: var(--light-grey);
}

.column.three {
  display: flex;
  /* gap: 10px; */
  justify-content: flex-end;
}

.bubble {
  border: var(--light-grey) 1px solid;
  border-radius: var(--border-containers);
  display: flex;
  flex-direction: column;
  width: 3.5em;
  height: 70%;
  text-align: center;
}

.bubble:first-child {
      margin-right: 10px;
  }

.bubble h3 {
  font-size: 40px;
  font-weight: 900;
  filter: drop-shadow(0px 2px 3px #979797);
}

@media screen and (min-width: 768px) {
  
  .column {
      flex: unset;
  }
  
  .column.one img {
      width: 275px;
      height: 275px
  }

  .column.two {
      overflow: unset;
      text-overflow: unset;
      display: unset;
      -webkit-line-clamp: unset;
      /* autoprefixer: ignore next */
      -webkit-box-orient: unset; 
  }

  .column.two h2 {
      font-size: var(--text-desktop-title);
      padding-bottom: 20px;
  }

  .column.three {
      position: absolute;
      right: 0;
      top: 30px;
  }

  .bubble {
      width: 4em;
      height: 80%;
  }

  .bubble:first-child {
      margin-right: 10px;
  }
}

</style>