<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-900 via-purple-900 to-gray-900 relative overflow-hidden">
    <!-- Animated Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute top-20 left-10 w-72 h-72 bg-gradient-to-r from-red-500/10 to-blue-500/10 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute bottom-20 right-10 w-96 h-96 bg-gradient-to-r from-purple-500/10 to-pink-500/10 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-gradient-to-r from-cyan-500/5 to-emerald-500/5 rounded-full blur-3xl animate-pulse"></div>
    </div>

    <div class="relative z-10 flex flex-col items-center justify-center p-6 min-h-screen">
      <!-- Header Section -->
      <div class="text-center py-16 max-w-5xl">
        <div class="mb-8">
          <h1 class="text-7xl font-extrabold bg-gradient-to-r from-red-400 via-purple-500 to-blue-500 bg-clip-text text-transparent mb-6 animate-pulse">
            About Us ✨ ◦
          </h1>
          <div class="w-32 h-1 bg-gradient-to-r from-red-500 to-blue-500 mx-auto rounded-full mb-8"></div>
        </div>
        
        <p class="text-xl text-gray-300 leading-relaxed max-w-3xl mx-auto mb-8">
          We're a passionate team of <span class="text-transparent bg-clip-text bg-gradient-to-r from-red-400 to-blue-400 font-semibold">Gen Z developers</span> 
          and creators building the future of web experiences. Our mission is to transform wild ideas into reality with cutting-edge technology and unlimited creativity! 🚀
        </p>

        <!-- Stats Section -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-6 mb-12">
          <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-2xl p-6 border border-gray-700/50 hover:border-red-500/50 transition-all duration-300 hover:scale-105">
            <div class="text-3xl font-bold text-red-400 mb-2">50+</div>
            <div class="text-gray-400 text-sm">Projects Done</div>
          </div>
          <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-2xl p-6 border border-gray-700/50 hover:border-blue-500/50 transition-all duration-300 hover:scale-105">
            <div class="text-3xl font-bold text-blue-400 mb-2">24/7</div>
            <div class="text-gray-400 text-sm">Support</div>
          </div>
          <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-2xl p-6 border border-gray-700/50 hover:border-purple-500/50 transition-all duration-300 hover:scale-105">
            <div class="text-3xl font-bold text-purple-400 mb-2">100%</div>
            <div class="text-gray-400 text-sm">Satisfaction</div>
          </div>
          <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-2xl p-6 border border-gray-700/50 hover:border-green-500/50 transition-all duration-300 hover:scale-105">
            <div class="text-3xl font-bold text-green-400 mb-2">3+</div>
            <div class="text-gray-400 text-sm">Years Exp</div>
          </div>
        </div>
      </div>

      <!-- Team Cards Section -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16 max-w-7xl">
        <!-- Team Member 1 -->
        <div class="group relative">
          <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-3xl p-8 border border-gray-700/50 hover:border-red-500/50 transition-all duration-500 hover:scale-110 hover:shadow-2xl hover:shadow-red-500/25 hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="w-40 h-40 mx-auto bg-gradient-to-br from-red-400 to-pink-600 rounded-full flex items-center justify-center text-6xl font-bold text-white shadow-2xl group-hover:animate-bounce">
                👨‍💻
              </div>
              <div class="absolute -top-3 -right-3 w-12 h-12 bg-green-500 rounded-full border-4 border-gray-800 flex items-center justify-center animate-pulse">
                <span class="text-white text-xs">🔥</span>
              </div>
              <!-- Skill badges -->
              <div class="absolute -bottom-2 left-1/2 transform -translate-x-1/2 flex space-x-2">
                <div class="bg-yellow-500 text-black text-xs px-2 py-1 rounded-full font-bold">JS</div>
                <div class="bg-blue-500 text-white text-xs px-2 py-1 rounded-full font-bold">Vue</div>
              </div>
            </div>
            <h3 class="text-2xl font-bold text-white mb-2 text-center">Alex Chen</h3>
            <p class="text-red-400 text-center mb-2 font-semibold">Frontend Wizard 🧙‍♂️</p>
            <p class="text-gray-400 text-center text-sm mb-6">Turning coffee into code since 2021</p>
            
            <!-- Social Links -->
            <div class="flex justify-center space-x-4 mb-4">
              <div class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-blue-500/50">
                <span class="text-white text-sm">💼</span>
              </div>
              <div class="w-10 h-10 bg-purple-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-purple-500/50">
                <span class="text-white text-sm">🐙</span>
              </div>
              <div class="w-10 h-10 bg-pink-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-pink-500/50">
                <span class="text-white text-sm">📱</span>
              </div>
            </div>

            <!-- Interactive Button -->
            <button class="w-full py-3 bg-gradient-to-r from-red-500 to-pink-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-red-500/50">
              Say Hi! 👋
            </button>
          </div>
        </div>

        <!-- Team Member 2 -->
        <div class="group relative">
          <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-3xl p-8 border border-gray-700/50 hover:border-blue-500/50 transition-all duration-500 hover:scale-110 hover:shadow-2xl hover:shadow-blue-500/25 hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="w-40 h-40 mx-auto bg-gradient-to-br from-blue-400 to-cyan-600 rounded-full flex items-center justify-center text-6xl font-bold text-white shadow-2xl group-hover:animate-bounce">
                👩‍🎨
              </div>
              <div class="absolute -top-3 -right-3 w-12 h-12 bg-green-500 rounded-full border-4 border-gray-800 flex items-center justify-center animate-pulse">
                <span class="text-white text-xs">✨</span>
              </div>
              <div class="absolute -bottom-2 left-1/2 transform -translate-x-1/2 flex space-x-2">
                <div class="bg-pink-500 text-white text-xs px-2 py-1 rounded-full font-bold">UI</div>
                <div class="bg-purple-500 text-white text-xs px-2 py-1 rounded-full font-bold">UX</div>
              </div>
            </div>
            <h3 class="text-2xl font-bold text-white mb-2 text-center">Sarah Kim</h3>
            <p class="text-blue-400 text-center mb-2 font-semibold">Design Goddess 🎨</p>
            <p class="text-gray-400 text-center text-sm mb-6">Making pixels perfect since forever</p>
            
            <div class="flex justify-center space-x-4 mb-4">
              <div class="w-10 h-10 bg-pink-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-pink-500/50">
                <span class="text-white text-sm">🎨</span>
              </div>
              <div class="w-10 h-10 bg-orange-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-orange-500/50">
                <span class="text-white text-sm">📱</span>
              </div>
              <div class="w-10 h-10 bg-cyan-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-cyan-500/50">
                <span class="text-white text-sm">💫</span>
              </div>
            </div>

            <button class="w-full py-3 bg-gradient-to-r from-blue-500 to-cyan-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-blue-500/50">
              Let's Create! 🚀
            </button>
          </div>
        </div>

        <!-- Team Member 3 -->
        <div class="group relative">
          <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-3xl p-8 border border-gray-700/50 hover:border-purple-500/50 transition-all duration-500 hover:scale-110 hover:shadow-2xl hover:shadow-purple-500/25 hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="w-40 h-40 mx-auto bg-gradient-to-br from-purple-400 to-indigo-600 rounded-full flex items-center justify-center text-6xl font-bold text-white shadow-2xl group-hover:animate-bounce">
                👨‍🔧
              </div>
              <div class="absolute -top-3 -right-3 w-12 h-12 bg-green-500 rounded-full border-4 border-gray-800 flex items-center justify-center animate-pulse">
                <span class="text-white text-xs">⚡</span>
              </div>
              <div class="absolute -bottom-2 left-1/2 transform -translate-x-1/2 flex space-x-2">
                <div class="bg-green-500 text-white text-xs px-2 py-1 rounded-full font-bold">API</div>
                <div class="bg-red-500 text-white text-xs px-2 py-1 rounded-full font-bold">DB</div>
              </div>
            </div>
            <h3 class="text-2xl font-bold text-white mb-2 text-center">Mike Rodriguez</h3>
            <p class="text-purple-400 text-center mb-2 font-semibold">Backend Beast 🦾</p>
            <p class="text-gray-400 text-center text-sm mb-6">Server whisperer & API architect</p>
            
            <div class="flex justify-center space-x-4 mb-4">
              <div class="w-10 h-10 bg-green-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-green-500/50">
                <span class="text-white text-sm">⚡</span>
              </div>
              <div class="w-10 h-10 bg-red-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-red-500/50">
                <span class="text-white text-sm">🔥</span>
              </div>
              <div class="w-10 h-10 bg-indigo-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-indigo-500/50">
                <span class="text-white text-sm">🛠️</span>
              </div>
            </div>

            <button class="w-full py-3 bg-gradient-to-r from-purple-500 to-indigo-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/50">
              Build Together! 🔧
            </button>
          </div>
        </div>

        <!-- Team Member 4 -->
        <div class="group relative">
          <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-3xl p-8 border border-gray-700/50 hover:border-green-500/50 transition-all duration-500 hover:scale-110 hover:shadow-2xl hover:shadow-green-500/25 hover:-translate-y-2">
            <div class="relative mb-6">
              <div class="w-40 h-40 mx-auto bg-gradient-to-br from-green-400 to-emerald-600 rounded-full flex items-center justify-center text-6xl font-bold text-white shadow-2xl group-hover:animate-bounce">
                👩‍💼
              </div>
              <div class="absolute -top-3 -right-3 w-12 h-12 bg-green-500 rounded-full border-4 border-gray-800 flex items-center justify-center animate-pulse">
                <span class="text-white text-xs">🎯</span>
              </div>
              <div class="absolute -bottom-2 left-1/2 transform -translate-x-1/2 flex space-x-2">
                <div class="bg-yellow-500 text-black text-xs px-2 py-1 rounded-full font-bold">PM</div>
                <div class="bg-teal-500 text-white text-xs px-2 py-1 rounded-full font-bold">Lead</div>
              </div>
            </div>
            <h3 class="text-2xl font-bold text-white mb-2 text-center">Emma Johnson</h3>
            <p class="text-green-400 text-center mb-2 font-semibold">Strategy Queen 👑</p>
            <p class="text-gray-400 text-center text-sm mb-6">Turning chaos into organized success</p>
            
            <div class="flex justify-center space-x-4 mb-4">
              <div class="w-10 h-10 bg-yellow-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-yellow-500/50">
                <span class="text-white text-sm">📊</span>
              </div>
              <div class="w-10 h-10 bg-teal-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-teal-500/50">
                <span class="text-white text-sm">🚀</span>
              </div>
              <div class="w-10 h-10 bg-emerald-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-emerald-500/50">
                <span class="text-white text-sm">💎</span>
              </div>
            </div>

            <button class="w-full py-3 bg-gradient-to-r from-green-500 to-emerald-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-green-500/50">
              Let's Plan! 📋
            </button>
          </div>
        </div>
      </div>

      <!-- Tagline Section -->
      <div class="text-center pb-16 max-w-5xl">
        <h2 class="text-5xl font-bold bg-gradient-to-r from-red-400 via-pink-500 to-blue-500 bg-clip-text text-transparent mb-8">
          We make sure your ideas & creations are delivered properly ✨
        </h2>
        <p class="text-xl text-gray-400 mb-12 leading-relaxed">
          From wild concepts to polished products, we're here to bring your vision to life with 
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-red-400 to-blue-400 font-semibold">passion, precision, and a lot of coffee</span> ☕
        </p>
        
        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row gap-6 justify-center mb-12">
          <button class="px-12 py-4 bg-gradient-to-r from-red-500 to-blue-500 text-white font-bold rounded-full hover:scale-110 transition-all duration-300 hover:shadow-2xl hover:shadow-purple-500/50 text-lg">
            Start Your Project 🚀
          </button>
          <button class="px-12 py-4 border-2 border-gray-600 text-white font-bold rounded-full hover:border-purple-500 hover:scale-110 transition-all duration-300 hover:shadow-2xl hover:shadow-purple-500/50 text-lg hover:bg-purple-500/10">
            View Our Work 👀
          </button>
        </div>

        <!-- Fun Facts -->
        <div class="bg-gradient-to-r from-gray-800/30 to-gray-900/30 backdrop-blur-lg rounded-3xl p-8 border border-gray-700/50">
          <h3 class="text-2xl font-bold text-white mb-6">Fun Facts About Us 🎉</h3>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-6 text-center">
            <div>
              <div class="text-4xl mb-2">☕</div>
              <div class="text-white font-semibold">1,247 cups of coffee consumed</div>
            </div>
            <div>
              <div class="text-4xl mb-2">🌙</div>
              <div class="text-white font-semibold">89 all-nighters pulled</div>
            </div>
            <div>
              <div class="text-4xl mb-2">🎵</div>
              <div class="text-white font-semibold">Lo-fi hip hop is our fuel</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
// No additional script logic needed for this static page
</script>

<style scoped>
/* Custom animations */
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

.animate-float {
  animation: float 3s ease-in-out infinite;
}

/* Hover glow effect */
.group:hover .shadow-2xl {
  box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.25), 0 0 0 1px rgba(255, 255, 255, 0.05);
}
</style>