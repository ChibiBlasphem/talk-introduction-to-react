<script setup lang="ts">
const props = defineProps({
  type: {
    type: String,
    default: "primary",
  },
});
</script>

<template>
  <div class="slidev-layout cover place-content-center" :class="props.type">
    <slot />
  </div>
</template>

<style scoped>
.cover {
  display: grid;
  align-items: center;
  justify-content: center;
}

.cover ::v-deep(*) {
  text-align: center;
}

.primary {
  background: #091927;
  color: #fff;
}

.secondary {
  background: #2d4358;
  color: #fff;
}

.tertiary {
  background: #8eacc6;
  color: #333;
}
</style>
