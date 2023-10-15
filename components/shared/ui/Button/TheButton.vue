<script setup lang="ts">
interface Props {
  btnClass?: string;
  btnStyle?: "accent";
}

const props = defineProps<Props>();
</script>
<template>
  <button :class="[$style.btn, props.btnClass, $style[props.btnStyle]]">
    <slot name="title"></slot>
  </button>
</template>
<style module lang="scss">
.btn {
  @apply py-6 border-accent border-[3px] text-xl font-semibold text-accent transition-colors bg-white uppercase;
}
.btn:hover {
  @apply bg-accent text-white;
}

.btn.accent {
  @apply bg-accent text-white hover:bg-transparent hover:text-accent;
}
</style>
