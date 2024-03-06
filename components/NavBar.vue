<template>
  <nav class="nav">
    <LogoHorizontal class="logo" :color="props.white ? 'white' : 'black'"></LogoHorizontal>

    <div class="buttons">
      <button
        @click="$router.push('/')"
        class="small translucent outline"
        :class="{ light: props.white }"
      >
        home
      </button>
      <button
        @click="$router.push('/about')"
        class="small translucent outline"
        :class="{ light: props.white }"
      >
        over
      </button>
      <button
        @click="$router.push('/shouts')"
        class="small translucent outline"
        :class="{ light: props.white }"
      >
        shouts
      </button>
    </div>
  </nav>
</template>

<script setup lang="ts">
const props = defineProps({
  white: Boolean,
});
</script>

<style lang="scss" scoped>
.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;

  width: 100vw;
  max-width: 100%;

  .logo {
    cursor: pointer;
    padding: 2rem;

    width: 300px;
  }

  .buttons {
    display: flex;
    gap: 0.5rem;

    padding: 0 2rem;
  }
}
</style>
