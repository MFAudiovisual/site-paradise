<template>
  <section id="home" class="home">
    <ParallaxStatic size="100vh" :image="image" :opacity="0.05">
      <template #title>
        <h1
          class="text-8xl font-montserrat uppercase font-normal drop-shadow-text-sm text-green-500/60 tracking-widest"
        >
          Natureza
        </h1>
      </template>
      <template #subtitle>
        <p
          class="text-gray-200 text-center uppercase tracking-widest relative mb-0 drop-shadow-text-sm"
        >
          PARADISE ENTRETENIMENTO
        </p>
        <div class="border-green-500/60 w-32 border-b-4 m-auto pt-4"></div>
      </template>
    </ParallaxStatic>
  </section>
</template>

<script setup>
import ParallaxStatic from '@/components/Sitesys/Global/Parallax/ParallaxStatic.vue'
import urlImage from '@/assets/images/sitesys/bg/bg-03.jpg'

const image = urlImage
</script>
