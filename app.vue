<template>
  <div class="content">
    <div class="keyboard">
      {{ ingredients.map(i => i.icon) }}
      <OtherChooser @addOther="addIngredient"/>
      <FruitsChooser class="fruits" @addFruit="addIngredient"/>
    </div>
  </div>
</template>
<script setup>
const ingredients = ref([])

const addIngredient= (ingredient) => {
  ingredients.value.push(ingredient)
}
</script>
<style lang="scss">
.content {
  width: 50%;
  margin: 0 auto;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

.fruits {
  margin-top: 20px;
}

.keyboard {
  justify-self: end;
}
</style>
