<template>
  <div class="menu">
    <NavBarButtons :light="props.light"></NavBarButtons>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{ light: Boolean }>();
</script>

<style lang="scss" scoped>
.menu {
  display: flex;
  gap: 0.75rem;

  padding: 0 2rem;
}
</style>
