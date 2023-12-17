<template>
  <div class="w-full">
    <div class="w-full grid grid-rows-1 md:grid-cols-12 pb-24 px-5">
      <div class="w-full md:col-span-5 col-span-full">
        <div class="w-full md:h-[590px] h-[343px] flex flex-col md:pt-[121px]">
          <div class="text-4xl tracking-widest font-light leading-[3.5rem]">
            Изготовление
          </div>
          <div class="text-4xl tracking-widest font-light leading-[3.5rem]">
            самодельного мыла
          </div>
          <div class="text-2xl font-light">с доставкой по России</div>
          <div class="pt-10">
            <button class="text-3xl font-extralight rounded-full tracking-widest border-2 border-[#88CCCB] py-2 px-6"
              @click="$router.push('/#catalog')">
              каталог
            </button>
          </div>
        </div>
      </div>
      <div class="max-w-[372px] md:max-w-none md:w-full md:h-[590px] h-[343px] md:col-span-7 col-span-full flex relative">
        <SoapCard class="lg:w-[349px] lg:h-[349px] md:h-[270px] md:w-[270px] w-[173px] h-[180px] absolute top-0 left-0"
          img="/soap_1.png" color="#FBD9DF" />
        <SoapCardBlurText class="absolute md:top-8 top-3 md:-left-28 left-24" text="большой выбор" />
        <SoapCard
          class="lg:w-[439px] lg:h-[399px] md:h-[349px] md:w-[349px] w-[218px] h-[206px] z-10 absolute bottom-0 right-0"
          img="/soap_2.png" color="#CCF0EF" />
        <SoapCardBlurText class="absolute md:bottom-[26px] bottom-6 md:left-[65px] z-20" text="качественные материалы" />
      </div>
    </div>
    <div class="w-full pb-24" id="about">
      <div class="tracking-widest font-normal md:text-5xl text-3xl text-center pb-[61px]">
        Преимущества нашей компании
      </div>
      <div class="w-full grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-7 px-5">
        <HeroCard class="justify-self-center" v-for="card in herocards" :key="card.title" :img="card.img"
          :text="card.text" :title="card.title" />
      </div>
    </div>
    <div class="w-full pb-24" id="contacts">
      <div class="tracking-widest font-normal md:text-5xl text-3xl text-center pb-[61px]">
        Контакты
      </div>
      <div class="w-full lg:px-[149px] px-[39px] flex flex-col gap-11">
        <div class="w-full flex lg:flex-row flex-col lg:rounded-full rounded-[30px] overflow-hidden">
          <div
            class="lg:w-1/2 flex justify-center text-3xl lg:text-4xl tracking-widest font-light leading-[3.5rem] py-5 lg:py-8 px-20 bg-[#CCF0F0]">
            телефон:
          </div>
          <div
            class="lg:w-1/2 flex justify-center text-2xl lg:text-3xl tracking-widest underline leading-[3.5rem] py-5 lg:py-8 bg-[#FBD9DF]">
            + 7 (922) 555-1234
          </div>
        </div>
        <div class="w-full flex lg:flex-row flex-col lg:rounded-full rounded-[30px] overflow-hidden">
          <div
            class="lg:w-1/2 flex justify-center items-center text-3xl lg:text-4xl tracking-widest font-light leading-[3.5rem] py-5 lg:py-8 px-20 bg-[#CCF0F0]">
            мессенджеры:
          </div>
          <div class="lg:w-1/2 flex justify-center items-center py-3 bg-[#FBD9DF]">
            <div class="w-full h-[55px] lg:h-[90px] flex justify-evenly">
              <img class="invert cursor-pointer" src="/vk.png" alt="" />
              <img class="invert cursor-pointer" src="/tg.png" alt="" />
              <img class="invert cursor-pointer" src="/wa.png" alt="" />
            </div>
          </div>
        </div>
        <div class="w-full flex lg:flex-row flex-col lg:rounded-full rounded-[30px] overflow-hidden">
          <div
            class="lg:w-1/2 flex justify-center text-3xl lg:text-4xl tracking-widest font-light whitespace-nowrap leading-[3.5rem] py-5 lg:py-8 px-20 bg-[#CCF0F0]">
            эл. почта:
          </div>
          <div
            class="lg:w-1/2 flex justify-center text-2xl lg:text-3xl tracking-widest underline leading-[3.5rem] py-5 lg:py-8 bg-[#FBD9DF]">
            johnsmith@ gmail
          </div>
        </div>
      </div>
    </div>
    <div class="w-full pb-24" id="review">
      <div class="tracking-widest font-normal md:text-5xl text-3xl text-center pb-[61px]">
        Отзывы
      </div>
      <HeroReviews />
    </div>
  </div>
</template>

<script lang="ts" setup>
const herocards = [
  {
    img: "/hero1.png",
    text: "мы используем только натуральные и органические ингредиенты в производстве нашего мыла, что делает его более безопасным и полезным для кожи.",
    title: "Натуральные ингредиенты",
  },
  {
    img: "/hero2.png",
    text: "каждый кусок нашего мыла изготавливается вручную с любовью и вниманием к деталям, что придает ему уникальный и индивидуальный характер.",
    title: "Ручное производство",
  },
  {
    img: "/hero3.png",
    text: "мы предлагаем широкий выбор различных видов мыла, от ароматических до травяных, чтобы каждый клиент мог найти подходящий ему вариант.",
    title: "Разнообразие ассортимента",
  },
  {
    img: "/hero4.png",
    text: "мы получаем много положительных отзывов от наших довольных клиентов, что свидетельствует о качестве и эффективности нашего продукта.",
    title: "Положительные отзывы клиентов",
  },
];

useHead({
  title: "Изготовление самодельного мыла с доставкой по России",
});
</script>
