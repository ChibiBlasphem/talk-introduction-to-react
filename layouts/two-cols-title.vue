<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
});
</script>

<template>
  <div
    class="slidev-layout two-columns-title w-full h-full grid grid-cols-2 gap-4"
  >
    <div class="title col-span-2 text-center" :class="props.class">
      <slot name="title" />
    </div>
    <div class="col-left" :class="props.class">
      <slot />
    </div>
    <div class="col-right" :class="props.class">
      <slot name="right" />
    </div>
  </div>
</template>

<style>
.two-columns-title {
  grid-template-rows: auto 1fr;
}
</style>
