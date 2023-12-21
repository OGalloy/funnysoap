<template>
  <div class="w-full md:w-[298px] flex flex-col rounded-xl border-2 border-[#50A1A0] pt-4 pl-5 pr-5 pb-6">
    <div class="flex justify-center items-center">
      <div class="flex justify-center items-center w-[118px] rounded-full bg-[#50A1A0] p-[18px]">
        <img class="w-full object-cover" :src="img" alt="soapPicture" />
      </div>
    </div>
    <div class="pt-[10px] text-center font-light text-black text-3xl">
      {{ title }}
    </div>
    <div class="mt-2 text-center text-xl font-extralight tracking-wide">
      {{ text }}
    </div>
  </div>
</template>

<script lang="ts" setup>
defineProps({
  img: {
    type: String,
    required: true
  },
  text: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  }
})
</script>

<style lang="scss"></style>
