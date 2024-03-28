<template>
  <div>
    <section class="section splash">
      <div class="hero indent">
        <span class="overline">Ontwikkeling met Vertrouwen</span>
        <h1 class="title">
          Wij ontwikkelen met passie <br />
          software op maat.
        </h1>

        <div class="cto">
          <button class="white">Contact</button>
          <button class="translucent light">Trotse Momenten</button>
        </div>
      </div>

      <img class="logo-part bottom" src="/logo_top_part.svg" alt="" />
    </section>

    <section class="section">
      <div class="indent">
        <span class="overline">Trotse Momenten</span>
        <h1 class="title small">
          Bekijk hier de opdrachten <br />
          waar we het meest trots op zijn.
        </h1>

        <div class="portfolio">
          <PortfolioPiece
            title="Healthy City Lab"
            description="WordPress Plugin voor plaatsen van content en gespecialiseerd styling-advies."
            image="https://images.unsplash.com/photo-1709377058964-929af7f2d02f?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
            :technique-icons="[siWordpress, siHtml5, siJavascript]"
          ></PortfolioPiece>

          <PortfolioPiece
            title="Healthy City Lab"
            description="WordPress Plugin voor plaatsen van content en gespecialiseerd styling-advies."
            image="https://images.unsplash.com/photo-1709377058964-929af7f2d02f?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
            :technique-icons="[siWordpress, siHtml5, siJavascript]"
          ></PortfolioPiece>
        </div>
      </div>

      <img class="logo-part top" src="/logo_bottom_part.svg" alt="" />
    </section>
  </div>
</template>

<script setup lang="ts">
import { siWordpress, siHtml5, siJavascript } from "simple-icons";
</script>

<style lang="scss" scoped>
.nav {
  position: absolute;
  top: 0;

  z-index: 1;
}

.hero {
  .cto {
    display: flex;
    gap: 1rem;

    button {
      max-width: 250px;
    }
  }
}

.portfolio {
  margin-top: 4rem;

  display: flex;
  flex-wrap: wrap;

  gap: 2rem;
}

.section {
  position: relative;

  width: 100vw;
  min-height: 100vh;
  max-width: 100%;

  overflow: hidden;

  &.splash {
    padding-top: 4rem;

    display: flex;
    align-items: center;

    color: white;
    background: rgb(var(--main-color-rgb));
  }
}

.logo-part {
  position: absolute;

  width: 25vw;

  &.bottom {
    bottom: 0;
    right: 0;
  }

  &.top {
    top: 0;
    right: 0;
  }
}
</style>
