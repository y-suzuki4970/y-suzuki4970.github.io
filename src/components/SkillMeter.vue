<script setup lang="ts">
import { computed } from "vue";

const props = defineProps<{ value: number }>();

const styles = computed(() => { 
  return {
    "--meter-value": props.value.toString()
  };
});

</script>

<template>
  <meter
    min="0"
    max="5"
    low="1"
    high="4"
    class="meter"
    :style="styles"
    :value="value"
  >
    {{ value }}%
  </meter>
</template>

<style scoped lang="scss">
@import "@/assets/styles/variables.scss";

.meter {
  position: relative;
  &::after {
    content: attr(value);
    position: absolute;
    top: 50%;
    left: 0;
    transform: translateY(-50%);
  }
  /*
  color: #eee;
  text-shadow: 2px 2px 4px #111, -2px -2px 4px #111;
  */
}
</style>
