<script setup lang="ts">
const props = defineProps({
  background: {
    type: String,
    default: "#2d4358",
  },
  color: {
    type: String,
    default: "#fff",
  },
});
</script>

<template>
  <div
    class="slidev-layout cover"
    :style="`background: ${props.background}; color: ${props.color};`"
  >
    <slot />
  </div>
</template>

<style scoped>
.cover {
  display: grid;
  align-items: center;
  justify-content: center;
}
</style>
