<script setup lang="ts">
interface Props {
  placeholder?: string;
  inputType?: "text" | "email" | "tel";
}

const props = defineProps<Props>();
</script>
<template>
  <div>
    <input
      :type="props.inputType ?? 'text'"
      :placeholder="props.placeholder ?? ''"
      :class="$style.input"
    />
  </div>
</template>

<style module lang="scss">
.input {
  @apply bg-white border-2 border-accent h-[58px]
    w-full px-6 py-4;
  @apply focus:shadow-none active:shadow-none focus:rounded-none focus:border-accent focus-visible:rounded-none focus-visible:shadow-none;
}
</style>
