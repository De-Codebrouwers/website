<template>
  <button class="button">
    <svg class="icon">
      <path :fill="props.light ? 'white' : 'black'" :d="mdiMenu"></path>
    </svg>
  </button>
</template>

<script setup lang="ts">
import { mdiMenu } from "@mdi/js";

const props = defineProps<{ light: Boolean }>();
</script>

<style lang="scss" scoped>
.button {
  max-width: 100px;

  .icon {
    width: 25px;
    height: 25px;
  }
}
</style>
