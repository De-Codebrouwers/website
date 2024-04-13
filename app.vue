<template>
  <NavBar @mobile-menu-clicked="sideNavExpanded = !sideNavExpanded"></NavBar>
  <SideNav
    @close="sideNavExpanded = false"
    :expanded="sideNavExpanded"
  ></SideNav>

  <NuxtPage />
</template>

<script setup lang="ts">
const sideNavExpanded = ref(false);

useHead({
  title: "De Codebrouwers",
  htmlAttrs: {
    lang: "nl-NL",
  },
  link: [
    {
      rel: "preconnect",
      href: "https://fonts.googleapis.com",
    },
    {
      rel: "preconnect",
      href: "https://fonts.gstatic.com",
      crossorigin: "anonymous",
    },
    {
      rel: "stylesheet",
      href: "https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap",
      crossorigin: "",
    },
  ],
});
</script>

<style lang="scss">
@import url("/assets/scss/main.scss");

html,
body {
  margin: 0;
  padding: 0;
}

.page-enter-active,
.page-leave-active {
  transition: opacity 0.3s;
  will-change: filter;
}
.page-enter-from,
.page-leave-to {
  opacity: 0;
}
</style>
