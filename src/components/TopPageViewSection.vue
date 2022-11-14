<script setup lang="ts">
const props = defineProps<{ enTitle?: string, jaTitle?: string, backgroundImageUrl: string }>();

</script>

<template>
  <section class="top-page-view_container" :style="`background-image: url(${props.backgroundImageUrl});`">
    <div class="top-page-view_content">
      <header v-if="enTitle || jaTitle" class="top-page-view_header">
        <h2>
          <span class="en-title">{{ props.enTitle }}</span>
          <span class="ja-title">{{ props.jaTitle }}</span>
        </h2>
      </header>
      <slot />
    </div>
  </section>
</template>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.top-page-view {
  &_container {
    background-size: cover;
    width: 100%;
    min-height: 100vh;
  }
  &_header {
    margin: 0 auto;
    padding-block-start: 1rem;
    padding-block-end: 1rem;
    width: $mainWidth;
    min-width: $minWidth;
    h2 {
      position: relative;
    }
  }
  &_content {
    min-height: 100vh;
    background-color: #eeea;
  }
}
.en-title {
  position: absolute;
  font-size: 2rem;
  top: 0;
  left: 0;
}
.ja-title {
  position: absolute;
  font-size: 1.25rem;
  top: 2rem;
  left: 2rem;
}
</style>
