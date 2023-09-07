<script setup lang="ts">
import { TheHeader } from "~/components/widjets/Header/";
import { TheFooter } from "~/components/widjets/Footer/";
</script>
<template>
  <div>
    <TheHeader />
    <slot />
    <TheFooter />
  </div>
</template>
