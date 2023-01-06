<script setup>
import SectionHome from '../components/Sitesys/Global/Sections/SectionHome.vue'
import SectionAbout from '../components/Sitesys/Global/Sections/SectionAbout.vue'
import SectionArtist from '../components/Sitesys/Global/Sections/SectionArtist.vue'
import SectionSport from '../components/Sitesys/Global/Sections/SectionSport.vue'
import SectionContact from '../components/Sitesys/Global/Sections/SectionContact.vue'
import ParallaxStatic from '../components/Sitesys/Global/Parallax/ParallaxStatic.vue'
import urlImage1 from '@/assets/images/sitesys/bg/bg-07.jpg'
import urlImage2 from '@/assets/images/sitesys/bg/bg-11.jpg'
import urlImage3 from '@/assets/images/sitesys/bg/bg-06.jpg'

const image1 = urlImage1
const image2 = urlImage2
const image3 = urlImage3
</script>

<template>
  <main>
    <SectionHome />
    <ParallaxStatic size="100vh" :image="image1" :opacity="0.01">
      <template #title>
        <h1
          class="text-8xl font-montserrat uppercase font-normal drop-shadow-text-sm text-green-500/60 tracking-widest"
        >
          Cultura
        </h1>
      </template>
      <template #subtitle>
        <p
          class="text-gray-200 text-center relative uppercase tracking-widest mb-0 drop-shadow-text-sm"
        >
          PARADISE ENTRETENIMENTO
        </p>
        <div class="border-green-500/60 w-32 border-b-4 m-auto pt-4"></div>
      </template>
    </ParallaxStatic>
    <ParallaxStatic size="100vh" :image="image2" :opacity="0.01">
      <template #title>
        <h1
          class="text-8xl font-montserrat uppercase font-normal drop-shadow-text-sm text-green-500/60 tracking-widest"
        >
          Música
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
    <ParallaxStatic size="100vh" :image="image3" :opacity="0.2">
      <template #title>
        <h1
          class="text-8xl font-montserrat uppercase font-normal drop-shadow-text-sm text-green-500/60 tracking-widest"
        >
          Esport
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
    <SectionAbout />
    <!-- Banner 1 -->
    <div
      class="my-36 bg-[url('/src/assets/images/sitesys/bg/bg-05.jpg')] bg-no-repeat bg-cover"
    >
      <div class="backdrop-opacity-50 bg-dark/60">
        <div class="container grid grid-cols-1 gap-4 py-32">
          <div
            class="text-dark text-lg font-bold font-amatic order-first md:order-last"
          >
            <h2
              id="section2"
              class="text-4xl text-light text-center font-normal font-amatic tracking-wide drop-shadow-text-md"
            >
              WELCOME TO PARADISE!
            </h2>
          </div>
        </div>
      </div>
    </div>
    <SectionArtist />
    <!-- Banner 2 -->
    <div
      class="my-36 bg-[url('/src/assets/images/sitesys/bg/bg-novidades-02.jpg')] bg-no-repeat bg-cover"
    >
      <div class="backdrop-opacity-50 bg-dark/60">
        <div class="container grid grid-cols-1 gap-4 py-32">
          <div
            class="text-dark text-lg font-bold font-amatic order-first md:order-last"
          >
            <h2
              id="section2"
              class="text-4xl text-light text-center font-normal font-amatic tracking-wide drop-shadow-text-md"
            >
              TENHA EXPERIÊNCIAS INCRÍVEIS!
            </h2>
          </div>
        </div>
      </div>
    </div>
    <SectionSport />
    <!-- Banner 2 -->
    <div
      class="my-36 bg-[url('/src/assets/images/sitesys/bg/bg-space.jpg')] bg-no-repeat bg-cover"
    >
      <div class="backdrop-opacity-50 bg-dark/60">
        <div class="container grid grid-cols-1 gap-4 py-32">
          <div
            class="text-dark text-lg font-bold font-amatic order-first md:order-last"
          >
            <h2
              id="section2"
              class="text-4xl text-light text-center font-normal font-amatic tracking-wide drop-shadow-text-md"
            >
              VAMOS EMBARCAR NESSA VIAGEM JUNTOS!?
            </h2>
          </div>
        </div>
      </div>
    </div>
    <SectionContact />
  </main>
</template>
