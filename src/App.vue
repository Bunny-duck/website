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
  <main class="pt-20">
    <RouterView />
  </main>

  <!-- Footer Section -->
  <footer class="bg-gradient-to-r from-gray-900 via-purple-900 to-gray-900 border-t border-gray-700/50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
        <!-- Company Info -->
        <div class="col-span-1 md:col-span-2">
          <div class="flex items-center space-x-3 mb-6">
            <img src="./assets/logo.svg" alt="Vue.js Logo" class="h-8 w-8">
            <h3 class="text-xl font-bold bg-gradient-to-r from-white to-gray-300 bg-clip-text text-transparent">
              Vue.js
            </h3>
          </div>
          <p class="text-gray-400 mb-6 leading-relaxed">
            Building the future of web development with cutting-edge technology and 
            <span class="text-transparent bg-clip-text bg-gradient-to-r from-purple-400 to-pink-400">creative innovation</span>. 
            Let's create something amazing together! ✨
          </p>
          <div class="flex space-x-4">
            <div class="w-10 h-10 bg-gradient-to-r from-purple-500 to-indigo-500 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-purple-500/50">
              <span class="text-white">🐙</span>
            </div>
            <div class="w-10 h-10 bg-gradient-to-r from-blue-500 to-cyan-500 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-blue-500/50">
              <span class="text-white">💼</span>
            </div>
            <div class="w-10 h-10 bg-gradient-to-r from-pink-500 to-red-500 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-pink-500/50">
              <span class="text-white">📱</span>
            </div>
          </div>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="text-lg font-semibold text-white mb-6">Quick Links</h4>
          <ul class="space-y-3">
            <li><RouterLink to="/" class="text-gray-400 hover:text-purple-400 transition-colors">🏠 Home</RouterLink></li>
            <li><RouterLink to="/about" class="text-gray-400 hover:text-purple-400 transition-colors">✨ About</RouterLink></li>
            <li><RouterLink to="/userlist" class="text-gray-400 hover:text-purple-400 transition-colors">👥 Team</RouterLink></li>
            <li><RouterLink to="/contact" class="text-gray-400 hover:text-purple-400 transition-colors">📧 Contact</RouterLink></li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div>
          <h4 class="text-lg font-semibold text-white mb-6">Get in Touch</h4>
          <ul class="space-y-3 text-gray-400">
            <li class="flex items-center space-x-2">
              <span>📧</span>
              <span>bunny@gmail.com</span>
            </li>
            <li class="flex items-center space-x-2">
              <span>📱</span>
              <span>+1 (555) 123-4567</span>
            </li>
            <li class="flex items-center space-x-2">
              <span>📍</span>
              <span>BP 511, Phum Tropeang Chhuk (Borey Sorla) Sangtak, Street 371, Phnom Penh</span>
            </li>
          </ul>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="border-t border-gray-700/50 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
        <p class="text-gray-400 text-sm">
          © 2024 Vue.js Company. Made with 💜 and lots of ☕
        </p>
        <div class="flex space-x-6 mt-4 md:mt-0">
          <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors text-sm">Privacy Policy</a>
          <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors text-sm">Terms of Service</a>
        </div>
      </div>
    </div>
  </footer>
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

<style scoped>
/* Active navigation link styles */
.nav-active {
  @apply bg-gradient-to-r from-white/20 to-white/10 backdrop-blur-lg border border-white/30 shadow-lg;
}

.nav-active span {
  @apply text-white font-bold;
}

/* Custom animations */
@keyframes glow {
  0%, 100% { box-shadow: 0 0 20px rgba(168, 85, 247, 0.3); }
  50% { box-shadow: 0 0 30px rgba(168, 85, 247, 0.6); }
}

.nav-active {
  animation: glow 2s ease-in-out infinite;
}

/* Smooth scroll behavior */
html {
  scroll-behavior: smooth;
}

/* Hide scrollbar but keep functionality */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: rgba(31, 41, 55, 0.5);
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(to bottom, #8b5cf6, #ec4899);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(to bottom, #7c3aed, #db2777);
}
</style>