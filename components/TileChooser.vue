<template>
  <div class="tile">
    {{ icon }} {{ name }}
  </div>
</template>

<script setup>
defineProps(
    {
      name: {
        type: String,
        required: true,
      },
      icon: {
        type: String,
        required: true,
      }
    })
</script>

<style lang="scss">
.tile {
  padding: 10px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 8px;
  box-shadow: 0px 10px 15px -3px rgba(0, 0, 0, 0.2);

  &:hover {
    cursor: pointer;
  }
}
</style>
