<script setup lang="ts"></script>

<template>
  <header class="py-4">
    <div class="ce-container">
      <div class="flex items-center justify-between">
        <div>
          <img src="@/assets/svg/logo-ce.svg" alt="logo" class="w-10 h-auto" />
        </div>

        <div class="flex items-center gap-10">
          <div class="flex items-center gap-7">
            <img
              src="@/assets/svg/telegram-icon.svg"
              alt="telegram"
              class="w-6 h-auto cursor-pointer"
            />
          </div>
          <div class="flex flex-col gap-2 w-[35px] cursor-pointer">
            <div class="bg-black h-[3px] w-full"></div>
            <div class="bg-black h-[3px] w-full"></div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>
