<template>
  <header class="flex items-center px-6 py-6 text-black">
    <nav class="flex w-full">
      <div class="w-full flex items-center">
        <div class="w-1/2 md:flex md:justify-evenly">
          <NuxtLink to="/" class="text-2xl">
            <img src="~/assets/logo.svg" />
          </NuxtLink>
          <NuxtLink v-for="link in links" :key="link.name" :to="link.path" class="text-2xl font-semibold hidden md:block">
            {{ link.name
            }}</NuxtLink>
        </div>
        <div class="w-full flex justify-end md:hidden">
          <button class="p-2 block rounded-md hover:bg-neutral-200 transition-colors duration-150" @click="isOpen = true">
            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>
      </div>

      <USlideover class="md:hidden" v-model="isOpen" :ui="overlayTheme" prevent-close>
        <div class="p-6 w-full flex flex-col">
          <div class="w-full flex justify-end">
            <button class="p-2 flex rounded-md hover:bg-neutral-800 transition-colors duration-150 text-center"
              @click="isOpen = false">
              <UIcon class="h-6 w-6" name="i-heroicons-x-mark-20-solid" />
            </button>
          </div>
          <NuxtLink @click="loadLink" v-for="link in links" :key="link.name" :to="link.path"
            class="text-2xl mb-2 font-semibold">{{
              link.name }}
          </NuxtLink>
        </div>
      </USlideover>
    </nav>
  </header>
</template>

<script lang="ts" setup>
const isOpen = ref(false);

const overlayTheme = ref({
  overlay: {
    background: "bg-neutral-200/75 dark:bg-neutral-800/75",
  },
  background: "bg-white dark:bg-neutral-900",
});

const links = [
  {
    name: "Каталог",
    path: "/catalog",
  },
  {
    name: "О нас",
    path: "/",
  },
  {
    name: "Контакты",
    path: "/",
  },
];

const loadLink = () => {
  isOpen.value = false;
}
</script>

<style scoped></style>
