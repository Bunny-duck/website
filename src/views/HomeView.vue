<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-900 via-purple-900 to-gray-900 flex flex-col items-center justify-center p-6">
    <!-- Header Section -->
    <div class="text-center py-16 max-w-4xl">
      <h1 class="text-6xl font-extrabold bg-gradient-to-r from-red-500 via-purple-500 to-blue-500 bg-clip-text text-transparent mb-6">
        Home page ✨ ◦
      </h1>
      <p class="text-xl text-gray-300 leading-relaxed max-w-2xl mx-auto">
        We're a passionate team of developers and creators building the future of web experiences. 
        Our mission is to transform ideas into reality with cutting-edge technology.
      </p>
    </div>

    <!-- Team Cards Section -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16 max-w-7xl">
      <!-- Team Member 1 -->
      <div class="group relative">
        <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-2xl p-6 border border-gray-700/50 hover:border-red-500/50 transition-all duration-500 hover:scale-105 hover:shadow-2xl hover:shadow-red-500/20">
          <div class="relative mb-6">
            <div class="w-32 h-32 mx-auto bg-gradient-to-br from-red-400 to-pink-600 rounded-full flex items-center justify-center text-4xl font-bold text-white shadow-lg">
              👨‍💻
            </div>
            <div class="absolute -top-2 -right-2 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-800 animate-pulse"></div>
          </div>
          <h3 class="text-xl font-bold text-white mb-2 text-center">Alex Chen</h3>
          <p class="text-gray-400 text-center mb-4">Frontend Developer</p>
          <div class="flex justify-center space-x-3">
            <div class="w-8 h-8 bg-blue-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform cursor-pointer">
              <span class="text-white text-sm">💼</span>
            </div>
            <div class="w-8 h-8 bg-purple-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform cursor-pointer">
              <span class="text-white text-sm">🐙</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Team Member 2 -->
      <div class="group relative">
        <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-2xl p-6 border border-gray-700/50 hover:border-blue-500/50 transition-all duration-500 hover:scale-105 hover:shadow-2xl hover:shadow-blue-500/20">
          <div class="relative mb-6">
            <div class="w-32 h-32 mx-auto bg-gradient-to-br from-blue-400 to-cyan-600 rounded-full flex items-center justify-center text-4xl font-bold text-white shadow-lg">
              👩‍🎨
            </div>
            <div class="absolute -top-2 -right-2 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-800 animate-pulse"></div>
          </div>
          <h3 class="text-xl font-bold text-white mb-2 text-center">Sarah Kim</h3>
          <p class="text-gray-400 text-center mb-4">UI/UX Designer</p>
          <div class="flex justify-center space-x-3">
            <div class="w-8 h-8 bg-pink-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform cursor-pointer">
              <span class="text-white text-sm">🎨</span>
            </div>
            <div class="w-8 h-8 bg-orange-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform cursor-pointer">
              <span class="text-white text-sm">📱</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Team Member 3 -->
      <div class="group relative">
        <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-2xl p-6 border border-gray-700/50 hover:border-purple-500/50 transition-all duration-500 hover:scale-105 hover:shadow-2xl hover:shadow-purple-500/20">
          <div class="relative mb-6">
            <div class="w-32 h-32 mx-auto bg-gradient-to-br from-purple-400 to-indigo-600 rounded-full flex items-center justify-center text-4xl font-bold text-white shadow-lg">
              👨‍🔧
            </div>
            <div class="absolute -top-2 -right-2 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-800 animate-pulse"></div>
          </div>
          <h3 class="text-xl font-bold text-white mb-2 text-center">Mike Rodriguez</h3>
          <p class="text-gray-400 text-center mb-4">Backend Engineer</p>
          <div class="flex justify-center space-x-3">
            <div class="w-8 h-8 bg-green-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform cursor-pointer">
              <span class="text-white text-sm">⚡</span>
            </div>
            <div class="w-8 h-8 bg-red-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform cursor-pointer">
              <span class="text-white text-sm">🔥</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Team Member 4 -->
      <div class="group relative">
        <div class="bg-gradient-to-br from-gray-800/50 to-gray-900/50 backdrop-blur-lg rounded-2xl p-6 border border-gray-700/50 hover:border-green-500/50 transition-all duration-500 hover:scale-105 hover:shadow-2xl hover:shadow-green-500/20">
          <div class="relative mb-6">
            <div class="w-32 h-32 mx-auto bg-gradient-to-br from-green-400 to-emerald-600 rounded-full flex items-center justify-center text-4xl font-bold text-white shadow-lg">
              👩‍💼
            </div>
            <div class="absolute -top-2 -right-2 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-800 animate-pulse"></div>
          </div>
          <h3 class="text-xl font-bold text-white mb-2 text-center">Emma Johnson</h3>
          <p class="text-gray-400 text-center mb-4">Product Manager</p>
          <div class="flex justify-center space-x-3">
            <div class="w-8 h-8 bg-yellow-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform cursor-pointer">
              <span class="text-white text-sm">📊</span>
            </div>
            <div class="w-8 h-8 bg-teal-600 rounded-full flex items-center justify-center hover:scale-110 transition-transform cursor-pointer">
              <span class="text-white text-sm">🚀</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Tagline Section -->
    <div class="text-center pb-16 max-w-4xl">
      <h2 class="text-4xl font-bold bg-gradient-to-r from-red-400 via-pink-500 to-blue-500 bg-clip-text text-transparent mb-6">
        We make sure your ideas & creations are delivered properly ✨
      </h2>
      <p class="text-lg text-gray-400 mb-8">
        From concept to deployment, we're here to bring your vision to life with passion and precision.
      </p>
      
      <!-- CTA Buttons -->
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <button class="px-8 py-4 bg-gradient-to-r from-red-500 to-blue-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/25">
          Get Started 🚀
        </button>
        <button class="px-8 py-4 border-2 border-gray-600 text-white font-semibold rounded-full hover:border-purple-500 hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/25">
          Learn More 📖
        </button>
      </div>
    </div>

    <!-- Floating Elements -->
    <div class="absolute top-20 left-10 w-20 h-20 bg-gradient-to-r from-red-500/20 to-blue-500/20 rounded-full blur-xl animate-pulse"></div>
    <div class="absolute bottom-20 right-10 w-32 h-32 bg-gradient-to-r from-purple-500/20 to-pink-500/20 rounded-full blur-xl animate-pulse"></div>
  </div>
</template>

<script setup>
// No additional script logic needed for this static page
</script>

<style scoped>
/* Custom animations */
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.group:hover .animate-float {
  animation: float 2s ease-in-out infinite;
}
</style>