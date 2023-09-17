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
  @apply bg-white appearance-none border-2 border-accent;
}
</style>
