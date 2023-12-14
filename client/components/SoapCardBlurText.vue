<template>
  <div class="w-fit rounded-[25px] overflow-hidden">
    <div
      class="h-fit tracking-widest font-extralight whitespace-nowrap px-3 md:py-4 py-2 backdrop-blur-sm bg-white/[55%]">
      <span class="md:text-2xl text-base">{{ text }}</span>
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps({
  text: {
    type: String,
    required: true
  }
})
</script>

<style lang="scss"></style>