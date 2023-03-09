<template>
  <button class="base-button">Test</button>
</template>

<script setup lang="ts">
type Props = {
  test: string;
};

defineProps<Props>();
</script>
<style lang="postcss">
.base-button {
  @apply text-green-600 font-bold
}
</style>
