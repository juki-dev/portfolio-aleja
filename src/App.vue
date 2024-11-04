<!-- App.vue -->
<template>
  <div class="min-h-screen bg-gray-50">
    <!-- Mobile Menu Button - Only visible on small screens -->
    <button 
      @click="toggleMobileMenu"
      class="lg:hidden fixed top-4 left-4 z-30 p-2 rounded-md bg-white shadow-lg"
    >
      <div class="w-6 h-6 relative">
        <span 
          class="block w-full h-0.5 bg-gray-600 transition-all duration-300"
          :class="{ 'rotate-45 translate-y-2.5': isMobileMenuOpen }"
        ></span>
        <span 
          class="block w-full h-0.5 bg-gray-600 my-2 transition-all duration-300"
          :class="{ 'opacity-0': isMobileMenuOpen }"
        ></span>
        <span 
          class="block w-full h-0.5 bg-gray-600 transition-all duration-300"
          :class="{ '-rotate-45 -translate-y-2.5': isMobileMenuOpen }"
        ></span>
      </div>
    </button>

    <!-- Sidebar - Full width on mobile when open, fixed on desktop -->
    <aside 
      :class="[
        'bg-white shadow-lg transition-all duration-300 z-20',
        'lg:fixed lg:w-64 lg:h-full lg:translate-x-0',
        isMobileMenuOpen 
          ? 'fixed inset-0 translate-x-0' 
          : 'fixed inset-0 -translate-x-full'
      ]"
    >
      <div class="p-4 pt-16 lg:pt-4">
        <pr-card>
          <pr-presentation />
        </pr-card>

        <pr-card>
          <pr-menu />
        </pr-card>
        <pr-skill />
      </div>
    </aside>

    <!-- Overlay for mobile menu -->
    <div 
      v-if="isMobileMenuOpen" 
      class="fixed inset-0 bg-black bg-opacity-50 z-10 lg:hidden"
      @click="toggleMobileMenu"
    ></div>

    <!-- Main Content -->
    <div 
      :class="[
        'transition-all duration-300',
        'lg:ml-64' // Only apply margin on large screens
      ]"
    >
      <!-- Header -->
      <header 
        class="h-16 bg-white shadow-sm fixed top-0 right-0 z-10 transition-all duration-300"
        :class="[
          'lg:left-64', // Only apply left offset on large screens
          'left-0' // Default left position for mobile
        ]"
      >
        <div class="h-full flex items-center justify-between px-6">
          <h1 class="text-2xl font-bold text-gray-800 ml-8 lg:ml-0 flex items-center">
            <pr-logo :logo="currentLogo"/>
            <span>
              {{ currentSectionTitle }}
            </span>
          </h1>
          <button 
            class="px-4 py-2 contact-button transition-colors"
            @click="handleContact"
          >
            Contact Me
          </button>
        </div>
      </header>

      <!-- Main Content Area -->
      <main class="p-4 mt-16 lg:p-6">
        <div class="space-y-4 lg:space-y-6 max-w-6xl mx-auto">
          <RouterView />
        </div>
      </main>
    </div>
  </div>
</template>

<script setup>
import PrCard from './components/core/PrCard.vue'
import PrMenu from './components/PrMenu.vue'
import PrSkill from './components/PrSkill.vue'
import PrPresentation from './components/PrPresentation.vue'
import PrLogo from './components/core/PrLogo.vue';

import { RouterView, useRoute } from 'vue-router'
import { ref, computed } from 'vue'

const route = useRoute()
// Mobile menu state
const isMobileMenuOpen = ref(false)

// Computed property for section title
const currentSectionTitle = computed(() => {
  return route.meta?.title || "skills" 
})

const currentLogo = computed(() => {
  return route.meta?.logo || "skills" 
})

// Methods
const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const handleContact = () => {
  // Add your contact logic here
  console.log('Contact button clicked')
}
</script>

<style scoped>
.contact-button {
    display: flex;
    align-items: center;
    background: #FFFFFF;
    box-shadow: 10px 15px 10px rgba(183, 183, 183, 0.3);
    border-radius: 10px;
    padding: 10px;
    text-decoration: none;
    color: black;
    font-weight: 300;
}
.contact-button:hover {
    background: gray;
    box-shadow: 10px 15px 10px rgba(183, 183, 183, 0.3);
    color: white;
}
</style>