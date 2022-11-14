<script setup lang="ts">
const props = defineProps<{ enTitle?: string, jaTitle?: string, backgroundImageUrl: string }>();

</script>

<template>
  <section
    class="
      top-page-view_container
      bg-cover w-full min-h-screen
    "
    :style="`background-image: url(${props.backgroundImageUrl});`"
  >
    <div
      class="top-page-view_content
        w-full min-h-screen
        bg-gray-300 bg-opacity-75
      "
    >
      <header
        v-if="enTitle || jaTitle"
        class="top-page-view_header
          my-0 mx-auto pt-4 pb-4
        "
      >
        <h2 class="relative">
          <span
            class="
              en-title
              absolute text-4xl top-0 left-0
            "
          >{{ props.enTitle }}</span>
          <span
            class="
            ja-title
              absolute text-2xl top-8 left-8
            "
          >{{ props.jaTitle }}</span>
        </h2>
      </header>
      <slot />
    </div>
  </section>
</template>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.top-page-view {
  &_header {
    width: $mainWidth;
    min-width: $minWidth;
  }
}
</style>
