<template>
  <div class="rounded-[20px] overflow-hidden" :style="{ 'background-color': color }">
    <img class="max-w-full h-full object-cover z-50 border-0" :src="img" alt="Soap image" />
  </div>
</template>

<script lang="ts" setup>
defineProps({
  img: {
    type: String,
    required: true,
  },
  color: {
    type: String,
    required: true,
  },
});
</script>

<style></style>
