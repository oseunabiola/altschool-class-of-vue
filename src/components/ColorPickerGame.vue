<template>
  <h1>Color Picker Game</h1>

  <div>{{ message }}</div>

  <button v-for="color in colors" :key="color" @click="matchColor(color)">
    {{ color }}
  </button>
</template>

<script>
import colorComposable from "../composables/color-manager";
export default {
  setup() {
    const { colors, message, matchColor } = colorComposable();
    return { colors, message, matchColor };
  },
};
</script>

<style></style>
