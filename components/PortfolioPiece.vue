<template>
  <div
    class="portfolio-piece"
    :style="{ backgroundImage: `url('${props.image}')` }"
  >
    <div class="content">
      <div class="header">
        <h3 class="headline">{{ props.title }}</h3>
        <span class="description">{{ description }}</span>
      </div>

      <div class="footer">
        <span class="more-info">Naar de casus</span>

        <div class="techniques">
          <svg
            v-for="icon of props.techniqueIcons"
            class="icon"
            v-html="icon.svg"
          ></svg>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { PropType } from "vue";

const props = defineProps({
  title: String,
  description: String,
  image: String,
  techniqueIcons: Array as PropType<{ svg: string }[]>,
});
</script>

<style scoped lang="scss">
$width: 250px;
$height: 250px;
$padding: 3rem;

.portfolio-piece {
  position: relative;
  z-index: 1;

  cursor: pointer;

  width: $width;
  height: $height;
  padding: $padding;

  background-repeat: no-repeat;
  background-position: center center;
  background-attachment: fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;

  color: white;

  border-radius: var(--main-border-radius);

  .headline {
    margin: 0;
    margin-bottom: 1rem;

    font-size: 2rem;
    font-weight: 700;
  }

  .content {
    display: flex;
    justify-content: space-between;
    flex-direction: column;

    height: 100%;

    position: relative;
    z-index: 2;
  }

  .footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;

    .more-info {
      transition: opacity 0.25s;
      opacity: 0;
    }

    .techniques {
      display: flex;
      gap: 0.5rem;

      font-size: 0.7rem;

      opacity: 1;
      will-change: opacity;
      transition: opacity 0.2s;

      .icon {
        fill: white;

        width: 25px;
        height: 25px;
      }
    }
  }

  &:hover {
    .footer {
      .more-info {
        opacity: 1;
      }

      .techniques {
        opacity: 0;
      }
    }

    &::after {
      background: rgba(var(--main-color-rgb), 0.8);
    }
  }

  &::after {
    content: "";
    z-index: 1;

    position: absolute;
    top: 0;
    left: 0;

    width: 100%;
    height: 100%;

    border-radius: var(--main-border-radius);
    backdrop-filter: blur(10px);

    transition: background 0.25s;
    background: rgba(0, 0, 0, 0.5);
  }
}
</style>
