<template>
  <nav :class="{ home: isHomePage }" class="nav">
    <LogoHorizontal
      class="logo"
      :color="isHomePage ? 'white' : 'black'"
    ></LogoHorizontal>

    <NavBarDesktopMenu v-if="isDesktop" :light="isHomePage" />
    <NavBarMobileMenu
      v-else
      @click="emit('mobileMenuClicked')"
      :light="isHomePage"
    />
  </nav>
</template>

<script setup lang="ts">
import { breakpointsTailwind, useBreakpoints } from "@vueuse/core";

const emit = defineEmits(["mobileMenuClicked"]);

const route = useRoute();
const router = useRouter();

const breakpoints = useBreakpoints(breakpointsTailwind);
const isDesktop = breakpoints.greaterOrEqual("lg");

const isHomePage = ref(route.path === "/");

// this is to account for the transition between the pages
// and the state of the home page nav bar and the other nav bars
router.afterEach((to, _) => {
  setTimeout(() => {
    isHomePage.value = to.path === "/";
  }, 300);
});
</script>

<style lang="scss" scoped>
.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;

  width: 100vw;
  max-width: 100%;

  &.home {
    position: absolute;
    z-index: 1;
  }

  .logo {
    cursor: pointer;
    padding: 2rem;

    width: 300px;
  }
}
</style>
