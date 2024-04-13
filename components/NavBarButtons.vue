<template>
  <button
    @click="
      $router.push('/');
      emit('click');
    "
    class="small translucent outline"
    :class="{ light: props.light }"
  >
    home
  </button>
  <button
    @click="
      $router.push('/about');
      emit('click');
    "
    class="small translucent outline"
    :class="{ light: props.light }"
  >
    over
  </button>
  <button
    @click="
      $router.push('/shouts');
      emit('click');
    "
    class="small translucent outline"
    :class="{ light: props.light }"
  >
    shout-outs
  </button>
</template>

<script setup lang="ts">
const props = defineProps<{ light: Boolean }>();
const emit = defineEmits(["click"]);
</script>

<style scoped></style>
