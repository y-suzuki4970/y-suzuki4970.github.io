<script setup lang="ts">
defineProps<{ headerText: string }>();
</script>

<template>
  <article
    class="
      mx-auto my-0
      w-4/5 min-w-fit
    "
  >
    <header
      class="
        mx-auto mt-4 mb-4
        text-center
      "
    >
      <h3 class="font-bold">{{ headerText }}</h3>
    </header>
    <section
      class="
        ml-8
      "
    >
      <slot />
    </section>
  </article>
</template>

<style scoped lang="scss">
</style>
