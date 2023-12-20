<template>
  <div class="relative">
    <details class="group">
      <summary class="flex cursor-pointer items-center gap-2 pb-1 text-gray-900 transition">
        <span class="text-2xl tracking-widest">Сортировка</span>

        <span class="transition group-open:-rotate-180">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
            class="h-4 w-4">
            <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5" />
          </svg>
        </span>
      </summary>

      <div class="z-50 group-open:absolute group-open:start-0 group-open:top-auto group-open:mt-2">
        <div class="w-96 rounded border border-gray-200 bg-white">
          <header class="flex items-center justify-between p-4">
            <span class="text-xl tracking-widest text-gray-700"> 0 Выбрано </span>
            <button type="button" class="text-xl tracking-widest text-gray-900 underline underline-offset-4">
              Очистить
            </button>
          </header>
          <ul class="space-y-3 border-t border-gray-200 p-4">
            <li>
              <label for="FilterInStock" class="inline-flex items-center gap-2">
                <input type="checkbox" id="FilterInStock" class="h-5 w-5 rounded border-gray-300" />

                <span class="text-xl tracking-widest font-medium text-gray-700">
                  В наличии (5+)
                </span>
              </label>
            </li>
            <li>
              <label for="FilterOutOfStock" class="inline-flex items-center gap-2">
                <input type="checkbox" id="FilterOutOfStock" class="h-5 w-5 rounded border-gray-300" />

                <span class="text-xl tracking-widest font-medium text-gray-700">
                  Нет в наличии (10+)
                </span>
              </label>
            </li>
          </ul>
        </div>
      </div>
    </details>
  </div>
</template>

<script lang="ts" setup>

</script>

<style lang="scss"></style>