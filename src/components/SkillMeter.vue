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
    class="
      meter relative
      after:absolute
      after:left-0 after:top-1/2 after:-translate-y-1/2
    "
    :style="styles"
    :value="value"
  >
    {{ value }}%
  </meter>
</template>

<style scoped lang="scss">
.meter {
  &::after {
    content: attr(value);
  }
}
</style>
