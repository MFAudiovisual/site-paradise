<script setup>
import imgUrl from '@/assets/images/sitesys/logo/logo-header-light.png'

const footer = defineProps({
  company: {
    type: String,
    default: 'Paradise Entretenimento',
  },
  logo: {
    type: String,
    default: imgUrl,
  },
  description: {
    type: String,
    default: 'Brief description of the company.',
  },
  email1: {
    type: String,
    default: 'contactsitesys@sitesys.com',
  },
  email2: {
    type: String,
    default: 'supportsitesys@sitesys.com',
  },
  address: {
    type: String,
    default: 'Company Address, 0000 - Company District',
  },
  phone1: {
    type: String,
    default: '99 99999-9999',
  },
  phone2: {
    type: String,
    default: '88 88888-8888',
  },
  facebook: {
    type: String,
    default: 'https://www.facebook.com/',
  },
  instagram: {
    type: String,
    default: 'https://www.instagram.com/',
  },
  youtube: {
    type: String,
    default: 'https://www.youtube.com/',
  },
})
</script>

<template>
  <footer class="z-10 bg-dark text-gray-300 pt-6 pb-6">
    <div class="flex justify-center">
      <p class="text-xs text-gray-400">
        All rights reserved by
        <span class="font-bold">@{{ footer.company }}</span> 2023
      </p>
    </div>
  </footer>
</template>

<style scoped></style>
