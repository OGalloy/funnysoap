<template>
  <div class="flex w-full min-h-screen flex-col bg-white text-black">
    <Header class="w-full" />
    <div class="px-0 md:px-4 w-full pt-4 flex justify-center">
      <div class="flex justify-center w-full max-w-7xl pt-10">
        <slot />
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style></style>
