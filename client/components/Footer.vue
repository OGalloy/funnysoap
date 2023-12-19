<template>
  <footer class="w-full">
    <div class="px-4 w-full pt-4 flex justify-center bg-[#FBD9DF]">
      <div class="flex justify-center w-full max-w-7xl pb-10">
        <div class="w-full grid grid-rows-1 md:grid-cols-9">
          <div class="w-full md:col-span-2">
            <img src="~/assets/logo.svg" />
          </div>
          <div class="w-full md:col-span-2 flex flex-col pt-5 md:pt-[41px] space-y-1">
            <NuxtLink v-for="link in links" :key="link.name" :to="link.path" class="text-4xl font-extralight">
              {{ link.name }}</NuxtLink>
          </div>
          <div class="w-full md:col-span-2 pt-5 md:pt-[41px]">
            <div class="w-full h-[55px] flex space-x-6">
              <img class="invert cursor-pointer" src="/vk.png" alt="" />
              <img class="invert cursor-pointer" src="/tg.png" alt="" />
              <img class="invert cursor-pointer" src="/wa.png" alt="" />
            </div>
            <div class="flex pt-3 text-2xl leading-[3.5rem] underline">
              + 7 (922) 555-1234
            </div>
            <div class="flex text-2xl leading-[3.5rem] underline">
              johnsmith@ gmail
            </div>
          </div>
          <div class="w-full md:col-span-3 pt-5 md:pt-[41px]">
            <img class="cursor-pointer object-cover w-full md:w-4/5 h-[136px] rounded-[15px] border-[#5A8A8A] border-2"
              src="/map.png" alt="" />
            <span class="text-sm font-semibold">Россия, Владимирская область, г. Судогда, ул. Вымышленная, д.
              5с2, офис 12.</span>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>
const links = [
  {
    name: "каталог",
    path: "/#catalog",
  },
  {
    name: "о нас",
    path: "/#about",
  },
  {
    name: "контакты",
    path: "/#contacts",
  },
  {
    name: "отзывы",
    path: "/#review",
  },
];
</script>

<style lang="scss"></style>
