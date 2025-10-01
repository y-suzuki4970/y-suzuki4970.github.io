<script setup lang="ts">
defineProps<{ rate: number }>();
</script>

<template>
  <div v-once style="display: none">
    <svg xmlns="http://www.w3.org/2000/svg" class="rate-svg svg-star">
      <symbol id="svgRateStar" viewbox="0 0 24 24">
        <path fill="orange" d="M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z" />
      </symbol>
    </svg>
    <svg xmlns="http://www.w3.org/2000/svg" class="rate-svg svg-star-outline">
      <symbol id="svgRateStarOutline" viewbox="0 0 24 24">
        <path fill="orange" d="M12,15.39L8.24,17.66L9.23,13.38L5.91,10.5L10.29,10.13L12,6.09L13.71,10.13L18.09,10.5L14.77,13.38L15.76,17.66M22,9.24L14.81,8.63L12,2L9.19,8.63L2,9.24L7.45,13.97L5.82,21L12,17.27L18.18,21L16.54,13.97L22,9.24Z" />
      </symbol>
    </svg>
  </div>
  <template v-for="i of 5" :key="i">
    <svg
      v-if="Math.round(rate) >= i"
      viewBox="0 0 24 24"
      class="rate-svg inline stroke-yellow-600 w-5"
    >
      <use xlink:href="#svgRateStar" />
    </svg>
    <svg
      v-if="Math.round(rate) < i"
      viewBox="0 0 24 24"
      class="rate-svg inline stroke-yellow-600 w-5"
    >
      <use xlink:href="#svgRateStarOutline" />
    </svg>
  </template>
</template>

<style scoped lang="scss">
.rate-svg {
  text-shadow: 2px 2px 2px #111, -1px -1px 2px #111;
}
</style>
