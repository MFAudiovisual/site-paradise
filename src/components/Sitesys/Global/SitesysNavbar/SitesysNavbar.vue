<template>
  <header id="header" class="header">
    <!-- Sitesys Navbar -->
    <nav class="fixed top-0 z-50 w-full">
      <div
        :class="[
          y >= 120 ? 'bg-opacity-60 backdrop-blur-sm' : 'bg-opacity-0 pt-6',
        ]"
        class="bg-dark px-4 pt-3 pb-2 transition-all duration-300"
      >
        <div class="container md:container-sm mx-auto">
          <!-- Navbar Content -->
          <div class="flex justify-between items-center">
            <!-- Navbar Logo -->
            <NavbarLogo @click="goToTop()"> </NavbarLogo>
            <!-- Desktop Navbar Menu -->
            <div class="flex">
              <div class="hidden sm:flex items-center space-x-8">
                <NavbarLink
                  v-for="item in navigation"
                  :key="item.name"
                  :active="item.current"
                  @click="handleGoToSection(item)"
                  preserve-scroll
                  class="text-[18px] tracking-wider drop-shadow-text-md"
                >
                  {{ item.name }}
                </NavbarLink>
              </div>
              <!-- Button Show Mobile Menu -->
              <div class="sm:hidden flex items-center mb-1 drop-shadow-text-md">
                <button @click="showMobileMenu = !showMobileMenu">
                  <svg
                    v-show="showMobileMenu"
                    class="w-8 h-8 text-gray-200 hover:text-white"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M4 6h16M4 12h16M4 18h16"
                    ></path>
                  </svg>
                  <svg
                    v-show="!showMobileMenu"
                    class="w-8 h-8 text-gray-300 hover:text-white"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M6 18L18 6M6 6l12 12"
                    ></path>
                  </svg>
                </button>
              </div>
              <!-- Dropdown Button -->
              <DropdownConfig class="ml-2 mb-1 drop-shadow-text-sm" />
            </div>
          </div>
        </div>
      </div>
      <!-- Mobile Navbar -->
      <div
        class="sm:hidden z-10 bg-dark space-y-2 p-4 transition-all duration-300"
        :class="[
          { hidden: showMobileMenu },
          y >= 200 ? 'bg-opacity-60 backdrop-blur-sm' : 'bg-opacity-0 pt-7',
        ]"
      >
        <SidebarLink
          v-for="item in navigation"
          :key="item.name"
          :active="item.current"
          :hover="true"
          @click="handleGoToSection(item)"
          preserve-scroll
          :class="[
            y >= 120
              ? ''
              : 'bg-opacity-0 hover:bg-opacity-0 focus:bg-opacity-0',
          ]"
        >
          {{ item.name }}
        </SidebarLink>
      </div>
      <button
        v-show="!showMobileMenu"
        @click="handleCloseNavbar"
        class="fixed w-full h-full -z-10 inset-0 bg-black opacity-50 cursor-default"
        tabindex="-1"
      ></button>
    </nav>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import NavbarLink from './inc/NavbarLink.vue'
import NavbarLogo from './inc/NavbarLogo.vue'
import SidebarLink from './inc/SidebarLink.vue'
import { goToSection, goToTop } from '@/utils/scroll.js'
import DropdownConfig from './inc/DropdownConfig.vue'
import { useWindowScroll } from '@vueuse/core'

const { y } = useWindowScroll()

const handleGoToSection = (item) => {
  navigation.value.forEach((e) => {
    e.current = false
  })
  item.current = true
  goToSection(item.href)
  handleCloseNavbar()
}

const handleGoToHeader = () => {
  navigation.value.forEach((e) => {
    e.current = false
  })
  goToTop()
  handleCloseNavbar()
}

const showMobileMenu = ref(true)

const handleCloseNavbar = () => {
  showMobileMenu.value = true
}

const navigation = ref([
  { name: 'Início', href: 'home', current: false },
  { name: 'Sobre', href: 'about', current: false },
  { name: 'Artistas', href: 'artist', current: false },
  { name: 'Esporte', href: 'sport', current: false },
  { name: 'Contatos', href: 'contact', current: false },
])
</script>
