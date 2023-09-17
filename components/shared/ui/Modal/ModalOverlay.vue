<script setup lang="ts">
defineEmits(["click"]);
</script>
<template>
  <div
    class="fixed w-full h-full bg-black bg-opacity-50 flex items-center justify-center z-20"
    @click.self="$emit('click')"
  >
    <slot name="content"></slot>
  </div>
</template>
