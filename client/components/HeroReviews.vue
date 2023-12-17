<template>
  <div class="w-full px-6">
    <div class="navigation-wrapper w-full">
      <div ref="container" class="keen-slider text-black">
        <div class="keen-slider__slide">
          <div class="w-full flex flex-col rounded-[30px] overflow-hidden">
            <div class="flex flex-row text-2xl tracking-widest font-light whitespace-nowrap py-5 px-5 bg-[#CCF0F0]">
              <div class="mr-4 h-[70px] w-[70px]">
                <img class="rounded-full object-cover bg-white" src="/user.png" />
              </div>
              <div class="flex flex-col justify-evenly">
                <div>Василий</div>
                <div class="-ml-1">
                  <img src="/stars.svg" alt="" />
                </div>
              </div>
            </div>
            <div class="flex justify-center text-sm tracking-widest py-5 px-5 bg-[#FBD9DF]">
              Я очень доволен покупкой самодельного мыла на этом сайте. Огромный
              выбор ароматов и видов мыла, отличное качество и быстрая доставка.
              Обязательно буду заказывать здесь еще и рекомендую всем друзьям!
            </div>
          </div>
        </div>
        <div class="keen-slider__slide">
          <div class="w-full flex flex-col rounded-[30px] overflow-hidden">
            <div class="flex flex-row text-2xl tracking-widest font-light whitespace-nowrap py-5 px-5 bg-[#CCF0F0]">
              <div class="mr-4 h-[70px] w-[70px]">
                <img class="rounded-full object-cover bg-white" src="/user.png" />
              </div>
              <div class="flex flex-col justify-evenly">
                <div>Василий</div>
                <div class="-ml-1">
                  <img src="/stars.svg" alt="" />
                </div>
              </div>
            </div>
            <div class="flex justify-center text-sm tracking-widest py-5 px-5 bg-[#FBD9DF]">
              Я очень доволен покупкой самодельного мыла на этом сайте. Огромный
              выбор ароматов и видов мыла, отличное качество и быстрая доставка.
              Обязательно буду заказывать здесь еще и рекомендую всем друзьям!
            </div>
          </div>
        </div>
        <div class="keen-slider__slide">
          <div class="w-full flex flex-col rounded-[30px] overflow-hidden">
            <div class="flex flex-row text-2xl tracking-widest font-light whitespace-nowrap py-5 px-5 bg-[#CCF0F0]">
              <div class="mr-4 h-[70px] w-[70px]">
                <img class="rounded-full object-cover bg-white" src="/user.png" />
              </div>
              <div class="flex flex-col justify-evenly">
                <div>Василий</div>
                <div class="-ml-1">
                  <img src="/stars.svg" alt="" />
                </div>
              </div>
            </div>
            <div class="flex justify-center text-sm tracking-widest py-5 px-5 bg-[#FBD9DF]">
              Я очень доволен покупкой самодельного мыла на этом сайте. Огромный
              выбор ароматов и видов мыла, отличное качество и быстрая доставка.
              Обязательно буду заказывать здесь еще и рекомендую всем друзьям!
            </div>
          </div>
        </div>
        <div class="keen-slider__slide">
          <div class="w-full flex flex-col rounded-[30px] overflow-hidden">
            <div class="flex flex-row text-2xl tracking-widest font-light whitespace-nowrap py-5 px-5 bg-[#CCF0F0]">
              <div class="mr-4 h-[70px] w-[70px]">
                <img class="rounded-full object-cover bg-white" src="/user.png" />
              </div>
              <div class="flex flex-col justify-evenly">
                <div>Василий</div>
                <div class="-ml-1">
                  <img src="/stars.svg" alt="" />
                </div>
              </div>
            </div>
            <div class="flex justify-center text-sm tracking-widest py-5 px-5 bg-[#FBD9DF]">
              Я очень доволен покупкой самодельного мыла на этом сайте. Огромный
              выбор ароматов и видов мыла, отличное качество и быстрая доставка.
              Обязательно буду заказывать здесь еще и рекомендую всем друзьям!
            </div>
          </div>
        </div>
        <div class="keen-slider__slide">
          <div class="w-full flex flex-col rounded-[30px] overflow-hidden">
            <div class="flex flex-row text-2xl tracking-widest font-light whitespace-nowrap py-5 px-5 bg-[#CCF0F0]">
              <div class="mr-4 h-[70px] w-[70px]">
                <img class="rounded-full object-cover bg-white" src="/user.png" />
              </div>
              <div class="flex flex-col justify-evenly">
                <div>Василий</div>
                <div class="-ml-1">
                  <img src="/stars.svg" alt="" />
                </div>
              </div>
            </div>
            <div class="flex justify-center text-sm tracking-widest py-5 px-5 bg-[#FBD9DF]">
              Я очень доволен покупкой самодельного мыла на этом сайте. Огромный
              выбор ароматов и видов мыла, отличное качество и быстрая доставка.
              Обязательно буду заказывать здесь еще и рекомендую всем друзьям!
            </div>
          </div>
        </div>
      </div>
      <UIcon name="i-material-symbols-arrow-back-ios-rounded" class="arrow arrow--left text-[#5A8A8A] md:-ml-9 -ml-5"
        dynamic :class="{ 'text-[#769f9f]': current === 0 }" @click="slider.prev()" />
      <UIcon name="i-material-symbols-arrow-forward-ios-rounded" class="arrow arrow--right text-[#5A8A8A] md:-mr-10 -mr-5"
        dynamic :class="{ 'text-[#769f9f]': current === 2 }" @click="slider.next()" />
    </div>
    <div v-if="slider" class="dots w-full">
      <button v-for="(_slide, idx) in dotHelper" @click="slider.moveToIdx(idx)"
        :class="{ dot: true, active: current === idx }" :key="idx"></button>
    </div>
  </div>
</template>

<script setup>
import { useKeenSlider } from "keen-slider/vue.es";
import "keen-slider/keen-slider.min.css";

const current = ref(0);
const [container, slider] = useKeenSlider({
  breakpoints: {
    "(min-width: 0px)": {
      slides: {
        perView: 1,
      },
    },
    "(min-width: 768px)": {
      slides: {
        perView: 2,
        spacing: 20,
      },
    },
    "(min-width: 1024px)": {
      slides: {
        perView: 3,
        spacing: 30,
      },
    },
  },
  initial: current.value,
  slideChanged: (s) => {
    current.value = s.track.details.rel;
  },
});

const dotHelper = computed(() =>
  slider.value
    ? [
      ...Array(
        slider.value.track.details.slides.length -
        slider.value.options.slides.perView +
        1
      ).keys(),
    ]
    : []
);
console.log(slider);
</script>

<style>
.keen-slider__slide {
  max-width: 364px !important;
}

.navigation-wrapper {
  position: relative;
}

.dots {
  display: flex;
  padding: 10px 0;
  justify-content: center;
}

.dot {
  border: none;
  width: 25px;
  height: 25px;
  background: #ffffff;
  border-radius: 50%;
  border-color: #000;
  border-style: solid;
  border-width: 2px;
  margin: 0 5px;
  padding: 5px;
  cursor: pointer;
}

.dot:focus {
  outline: none;
}

.dot.active {
  background: #5A8A8A;
}

.arrow {
  width: 30px;
  height: 30px;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  -webkit-transform: translateY(-50%);
  fill: #fff;
  cursor: pointer;
}

.arrow--left {
  left: 5px;
}

.arrow--right {
  left: auto;
  right: 5px;
}
</style>
