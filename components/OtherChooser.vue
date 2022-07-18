<template>
  <div class="others">
    <TileChooser  v-for="(other, index) in others" :key="index" :name="other.name" :icon="other.icon" @click="addOther(other)"/>
  </div>
</template>


<script setup>
import {others} from "../data/others";
const emit = defineEmits()

function addOther(other) {
  emit('addOther', other)
}
</script>

<style lang="scss">
.others {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
  font-size: 1.5em;
}
</style>
