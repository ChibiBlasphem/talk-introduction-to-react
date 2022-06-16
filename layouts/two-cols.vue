<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
});
</script>

<template>
  <div class="slidev-layout two-columns w-full h-full grid grid-cols-2 gap-4">
    <div class="col-left overflow-y-auto" :class="props.class">
      <slot />
    </div>
    <div class="col-right overflow-y-auto" :class="props.class">
      <slot name="right" />
    </div>
  </div>
</template>
