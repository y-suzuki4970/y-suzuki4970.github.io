<script setup lang="ts">
const props = defineProps<{
  enTitle?: string,
  jaTitle?: string,
  backgroundImageUrl: string
  backgroundImageName?: string
  backgroundImageAuthor?: string
  backgroundImageSourceLink?: string
}>();

</script>

<template>
  <section
    class="
      top-page-view_container
      relative
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
    <aside
      class="
        absolute
        right-0 bottom-0
        p-2
        text-right
      "
    >
      <template v-if="backgroundImageName">
        <div v-if="backgroundImageSourceLink">Photo: <a :href="backgroundImageSourceLink" target="_blank" rel="noopener noreferrer">{{ backgroundImageName }}</a></div>
        <div v-else>Photo: {{ backgroundImageName }}</div>
      </template>
      <template v-if="backgroundImageAuthor">
        <div v-if="backgroundImageSourceLink">Photo: <a :href="backgroundImageSourceLink" target="_blank" rel="noopener noreferrer">{{ backgroundImageAuthor }}</a></div>
        <div v-else>撮影: {{ backgroundImageAuthor }}</div>
      </template>
    </aside>
  </section>
</template>

<style scoped lang="scss">
@use "@/assets/styles/variables";

.top-page-view {
  &_header {
    width: variables.$mainWidth;
    min-width: variables.$minWidth;
  }
}
</style>
