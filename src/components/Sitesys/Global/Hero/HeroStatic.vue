<template>
  <div
    class="relative overflow-hidden bg-no-repeat bg-cover bg-center"
    :style="{
      backgroundImage: `url(${image})`,
      height: size,
    }"
  >
    <div
      class="absolute top-0 right-0 bottom-0 left-0 w-full h-full overflow-hidden bg-fixed"
      :style="{
        backgroundColor: backgroundColor,
      }"
    >
      <div class="flex justify-center items-center h-full">
        <div class="text-center text-white px-6 md:px-12">
          <h2
            class="text-brand text-7xl md:text-8xl font-bold drop-shadow-lg tracking-tight mt-10 mb-4"
          >
            {{ title }}
          </h2>
          <p
            class="text-2xl md:text-3xl text-gray-200 font-semibold drop-shadow-md mb-16"
          >
            {{ description }}
          </p>
          <a
            :href="actionUrl"
            target="_blank"
            class="inline-flex items-center justify-center h-10 w-auto m-2 px-7 py-7 text-xl font-semibold leading-6 text-gray-200 whitespace-no-wrap bg-brand rounded shadow-sm hover:bg-brand-700 focus:outline-none focus:shadow-none overflow-hidden"
          >
            <div class="mr-2">
              <svg
                class="w-5 h-5"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M13 10V3L4 14h7v7l9-11h-7z"
                ></path>
              </svg>
            </div>
            <span class="relative"> Call Action </span>
            <div class="ml-2">
              <svg
                class="w-5 h-5"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M13 10V3L4 14h7v7l9-11h-7z"
                ></path>
              </svg>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import imgUrl from '@/assets/images/sitesys/hero/hero.png'

defineProps({
  image: {
    type: String,
    default: imgUrl, // Random image "https://placeimg.com/500/300/nature?t=" + Math.random()
  },
  size: {
    type: String,
    default: '76vh',
  },
  backgroundColor: {
    type: String,
    default: '#00000033',
  },
  opacity: {
    type: Number,
    default: 0.1,
  },
  title: {
    type: String,
    default: 'Hero Title',
  },
  description: {
    type: String,
    default: 'Hero Short Description',
  },
  actionLabel: {
    type: String,
    default: 'Hero Action',
  },
  actionUrl: {
    type: String,
    default: '/',
  },
})
</script>
