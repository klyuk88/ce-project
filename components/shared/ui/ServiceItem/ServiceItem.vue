<script setup lang="ts">
import { TheButton } from "~/components/shared/ui/Button/";

const props = defineProps<{
  price?: string;
  title?: string;
}>();
</script>
<template>
  <div class="rounded-[25px] bg-neutral-900 border-[1px] border-white">
    <div class="grid grid-cols-2 text-white">
      <div
        class="flex flex-col justify-between p-8 relative border-r-[1px] border-white"
      >
        <h3 class="uppercase text-[30px] w-[80%]">{{ props.title ?? "F" }}</h3>
        <div>
          <h4 class="uppercase text-xl">
            Стоимость {{ props.price ?? "0" }} руб./час
          </h4>
          <TheButton :btn-class="$style.btn" :btn-style="'accent'">
            <template #title> Консультация </template>
          </TheButton>
        </div>
      </div>
      <div class="p-8">
        <slot name="description"></slot>
        <div class="mt-10">
          <h6 class="font-medium uppercase">Технологии</h6>
          <div class="mt-3">
            <slot name="technologies"></slot>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style module lang="scss">
.btn {
  @apply py-3 px-0 w-[260px] mt-6 text-[18px];
}
</style>
