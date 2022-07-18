<template>
  <div class="fruits">
    <TileChooser  v-for="(fruit, index) in fruits" :key="index" :name="fruit.name" :icon="fruit.icon" @click="addFruit(fruit)"/>
  </div>
</template>

<script setup>
import {fruits} from "../data/fruits";
const emit = defineEmits()

function addFruit (fruit) {
  emit('addFruit', fruit)
}
</script>

<style lang="scss">
.fruits {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
  font-size: 1.5em;

  &__item {
    padding: 10px;
    border: 1px solid rgba(0,0,0,0.1);
    border-radius: 8px;
    box-shadow: 0px 10px 15px -3px rgba(0,0,0,0.2);

    &:hover {
      cursor: pointer;
    }
  }
}
</style>
