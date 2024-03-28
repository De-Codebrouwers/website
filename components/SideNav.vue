<template>
  <div :class="{ expanded: props.expanded }" class="side-nav">
    <span class="overline">menu</span>

    <div class="buttons">
      <NavBarButtons @click="emit('close')" :light="false"></NavBarButtons>
    </div>
  </div>

  <div
    @click="emit('close')"
    class="overlay"
    :class="{ expanded: props.expanded }"
  ></div>
</template>

<script setup lang="ts">
const props = defineProps<{ expanded: Boolean }>();
const emit = defineEmits(["close"]);
</script>

<style lang="scss" scoped>
.side-nav {
  position: fixed;
  z-index: 3;

  top: 0;
  right: 0;

  width: 35vw;
  height: 100vh;

  background-color: white;

  transform: scaleX(0);
  transform-origin: right center;
  transition: transform 0.3s;

  padding: 2rem;

  .buttons {
    display: flex;
    flex-direction: column;
    gap: 2rem;

    margin-top: 4rem;
  }

  &.expanded {
    transform: scaleX(1);
  }
}

.overlay {
  visibility: hidden;

  position: fixed;
  z-index: 2;

  content: "";

  top: 0;
  left: 0;

  width: 100vw;
  height: 100vh;

  background-color: rgba(0, 0, 0, 0.75);

  cursor: pointer;

  transition: all 0.3s;
  opacity: 0;

  will-change: backdrop-filter;

  &.expanded {
    visibility: visible;

    backdrop-filter: blur(0.25rem);
    opacity: 1;
  }
}
</style>
