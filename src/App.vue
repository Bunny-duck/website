<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref, onMounted, onUnmounted } from 'vue'

// Scroll state
const isScrolled = ref(false)

// Handle scroll events
const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header 
    :class="[
      'fixed top-0 left-0 right-0 z-50 transition-all duration-500',
      isScrolled 
        ? 'bg-gray-900/95 backdrop-blur-xl shadow-2xl shadow-purple-500/20 border-b border-gray-700/50' 
        : 'bg-gradient-to-r from-blue-900 to-purple-600 shadow-lg'
    ]"
  >
    <div class="wrapper max-w-8xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
      <!-- Logo Section -->
      <div class="logo flex items-center space-x-3 group">
        <div class="relative">
          <img 
            src="./assets/logo.svg" 
            alt="Vue.js Logo" 
            class="h-10 w-10 transition-transform duration-300 group-hover:scale-110 group-hover:rotate-12"
          >
          <div class="absolute inset-0 bg-gradient-to-r from-green-400 to-blue-500 rounded-full opacity-0 group-hover:opacity-20 transition-opacity duration-300 blur-sm"></div>
        </div>
        <h3 class="text-2xl font-bold bg-gradient-to-r from-white to-gray-200 bg-clip-text text-transparent group-hover:from-green-400 group-hover:to-blue-400 transition-all duration-300">
          Vue
        </h3>
      </div>

      <!-- Desktop Navigation -->
      <nav class="hidden md:flex space-x-2">
        <RouterLink 
          to="/" 
          class="relative px-6 py-3 text-white font-medium transition-all duration-300 rounded-full group overflow-hidden"
          :class="{ 'nav-active': $route.path === '/' }"
        >
          <span class="relative z-10 flex items-center space-x-2">
            <span>🏠</span>
            <span>Home</span>
          </span>
          <div class="absolute inset-0 bg-gradient-to-r from-pink-500 to-red-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-full"></div>
          <div class="absolute inset-0 bg-gradient-to-r from-pink-500/20 to-red-500/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-full blur-xl"></div>
        </RouterLink>
        
        <RouterLink 
          to="/about" 
          class="relative px-6 py-3 text-white font-medium transition-all duration-300 rounded-full group overflow-hidden"
          :class="{ 'nav-active': $route.path === '/about' }"
        >
          <span class="relative z-10 flex items-center space-x-2">
            <span>✨</span>
            <span>About</span>
          </span>
          <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-cyan-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-full"></div>
          <div class="absolute inset-0 bg-gradient-to-r from-blue-500/20 to-cyan-500/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-full blur-xl"></div>
        </RouterLink>
        
        <RouterLink 
          to="/userlist" 
          class="relative px-6 py-3 text-white font-medium transition-all duration-300 rounded-full group overflow-hidden"
          :class="{ 'nav-active': $route.path === '/userlist' }"
        >
          <span class="relative z-10 flex items-center space-x-2">
            <span>👥</span>
            <span>Team</span>
          </span>
          <div class="absolute inset-0 bg-gradient-to-r from-purple-500 to-indigo-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-full"></div>
          <div class="absolute inset-0 bg-gradient-to-r from-purple-500/20 to-indigo-500/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-full blur-xl"></div>
        </RouterLink>
        
        <RouterLink 
          to="/contact" 
          class="relative px-6 py-3 text-white font-medium transition-all duration-300 rounded-full group overflow-hidden"
          :class="{ 'nav-active': $route.path === '/contact' }"
        >
          <span class="relative z-10 flex items-center space-x-2">
            <span>📧</span>
            <span>Contact</span>
          </span>
          <div class="absolute inset-0 bg-gradient-to-r from-green-500 to-emerald-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-full"></div>
          <div class="absolute inset-0 bg-gradient-to-r from-green-500/20 to-emerald-500/20 opacity-0 group-hover:opacity-100 transition-opacity duration-300 rounded-full blur-xl"></div>
        </RouterLink>
      </nav>

      <!-- Mobile Menu Button -->
      <button 
        @click="mobileMenuOpen = !mobileMenuOpen"
        class="md:hidden relative w-10 h-10 bg-gradient-to-r from-pink-500 to-purple-500 rounded-full flex items-center justify-center hover:scale-110 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/50"
      >
        <span class="text-white text-xl">☰</span>
      </button>
    </div>

    <!-- Mobile Navigation -->
    <div 
      v-if="mobileMenuOpen"
      class="md:hidden bg-gray-900/95 backdrop-blur-xl border-t border-gray-700/50"
    >
      <nav class="px-4 py-6 space-y-4">
        <RouterLink 
          to="/" 
          @click="mobileMenuOpen = false"
          class="flex items-center space-x-3 px-4 py-3 text-white font-medium transition-all duration-300 rounded-2xl hover:bg-gradient-to-r hover:from-pink-500/20 hover:to-red-500/20"
          :class="{ 'bg-gradient-to-r from-pink-500/30 to-red-500/30 border border-pink-500/50': $route.path === '/' }"
        >
          <span class="text-2xl">🏠</span>
          <span>Home</span>
        </RouterLink>
        
        <RouterLink 
          to="/about" 
          @click="mobileMenuOpen = false"
          class="flex items-center space-x-3 px-4 py-3 text-white font-medium transition-all duration-300 rounded-2xl hover:bg-gradient-to-r hover:from-blue-500/20 hover:to-cyan-500/20"
          :class="{ 'bg-gradient-to-r from-blue-500/30 to-cyan-500/30 border border-blue-500/50': $route.path === '/about' }"
        >
          <span class="text-2xl">✨</span>
          <span>About</span>
        </RouterLink>
        
        <RouterLink 
          to="/userlist" 
          @click="mobileMenuOpen = false"
          class="flex items-center space-x-3 px-4 py-3 text-white font-medium transition-all duration-300 rounded-2xl hover:bg-gradient-to-r hover:from-purple-500/20 hover:to-indigo-500/20"
          :class="{ 'bg-gradient-to-r from-purple-500/30 to-indigo-500/30 border border-purple-500/50': $route.path === '/userlist' }"
        >
          <span class="text-2xl">👥</span>  
          <span>Team</span>
        </RouterLink>
        
        <RouterLink 
          to="/contact" 
          @click="mobileMenuOpen = false"
          class="flex items-center space-x-3 px-4 py-3 text-white font-medium transition-all duration-300 rounded-2xl hover:bg-gradient-to-r hover:from-green-500/20 hover:to-emerald-500/20"
          :class="{ 'bg-gradient-to-r from-green-500/30 to-emerald-500/30 border border-green-500/50': $route.path === '/contact' }"
        >
          <span class="text-2xl">📧</span>
          <span>Contact</span>
        </RouterLink>
      </nav>
    </div>
  </header>

  <!-- Main Content with top padding to account for fixed header -->
  <!-- <main class="pt-20"> -->
    <RouterView />
  <!-- </main> -->

  <!-- Footer Section -->
  
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const mobileMenuOpen = ref(false)
    
    return {
      mobileMenuOpen
    }
  }
}
</script>


