<template>
  <ClientOnly>
    <swiper-container ref="swiperRef" :init="false" :slides-per-view="2" class="overflow-hidden relative">
      <swiper-slide class="mr-10 swiper-slide">
        <!--        <NuxtLink :to="`/catalog/${recommendCard.id}`">-->
        <div class="flex gap-5 justify-between">
          <div class="border text-center">
            <NuxtImg :src="img" class=""/>
          </div>
        </div>
        <!--        </NuxtLink>-->
      </swiper-slide>
      <swiper-slide class="mr-10 swiper-slide">
        <!--        <NuxtLink :to="`/catalog/${recommendCard.id}`">-->
        <div class="flex gap-5 justify-between">
          <div class="border text-center">
            <NuxtImg :src="img" class=""/>
          </div>
        </div>
        <!--        </NuxtLink>-->
      </swiper-slide>
      <swiper-slide class="mr-10 swiper-slide">
        <!--        <NuxtLink :to="`/catalog/${recommendCard.id}`">-->
        <div class="flex gap-5 justify-between">
          <div class="border text-center">
            <NuxtImg :src="img" class=""/>
          </div>
        </div>
        <!--        </NuxtLink>-->
      </swiper-slide>
      <swiper-slide class="mr-10 swiper-slide">
        <!--        <NuxtLink :to="`/catalog/${recommendCard.id}`">-->
        <div class="flex gap-5 justify-between">
          <div class="border text-center">
            <NuxtImg :src="img" class=""/>
          </div>
        </div>
        <!--        </NuxtLink>-->
      </swiper-slide>
    </swiper-container>
  </ClientOnly>
</template>

<script lang="ts" setup>


const img = 'https://img.freepik.com/free-vector/clean-style-modern-business-card-template_1017-30352.jpg?semt=ais_hybrid&w=740&q=80'

const swiperRef = ref<any>()

const swiper = useSwiper(swiperRef, {
  effect: 'slide',
  loop: true,
  autoplay: {
    delay: 300
  },
  pagination: {
    el: '.swiper-pagination',
  },
  navigation: {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev',
  },
  breakpoints: {
    200: {
      slidesPerView: 1.5,
      spaceBetween: 20
    },
    // when window width is >= 320px
    320: {
      slidesPerView: 2.5,
      spaceBetween: 20
    },
    // when window width is >= 480px
    480: {
      slidesPerView: 3.5,
      spaceBetween: 30
    },
    1020: {
      slidesPerView: 5.5,
      spaceBetween: 40
    },
    // when window width is >= 640px
    1280: {
      slidesPerView: 7.5,
      spaceBetween: 40
    }
  }
})
</script>

<style>
.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;
  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
