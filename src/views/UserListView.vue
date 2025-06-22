<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-900 via-purple-900 to-gray-900 relative overflow-hidden">
    <!-- Animated Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute top-10 left-10 w-96 h-96 bg-gradient-to-r from-red-500/10 to-pink-500/10 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute bottom-10 right-10 w-80 h-80 bg-gradient-to-r from-blue-500/10 to-cyan-500/10 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-64 h-64 bg-gradient-to-r from-purple-500/5 to-indigo-500/5 rounded-full blur-3xl animate-pulse"></div>
    </div>

    <div class="relative z-10 p-6">
      <!-- Header Section -->
      <div class="text-center py-16 max-w-5xl mx-auto">
        <h1 class="text-7xl font-extrabold bg-gradient-to-r from-red-400 via-purple-500 to-blue-500 bg-clip-text text-transparent mb-8 animate-pulse">
          Our Amazing Team ✨ ◦
        </h1>
        <div class="w-32 h-1 bg-gradient-to-r from-red-500 to-blue-500 mx-auto rounded-full mb-8"></div>
        <p class="text-xl text-gray-300 leading-relaxed max-w-3xl mx-auto mb-12">
          Meet the incredible minds behind our success! Each team member brings unique skills and 
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-red-400 to-blue-400 font-semibold">unstoppable creativity</span> 
          to every project we tackle together 🚀
        </p>

        <!-- View Toggle and Filter Buttons -->
        <div class="flex flex-col lg:flex-row justify-between items-center gap-6 mb-12">
          <!-- View Toggle -->
          <div class="flex bg-gray-800/50 backdrop-blur-lg rounded-full p-2 border border-gray-700/50">
            <button 
              @click="viewMode = 'cards'"
              :class="[
                'px-6 py-3 rounded-full font-semibold transition-all duration-300',
                viewMode === 'cards' 
                  ? 'bg-gradient-to-r from-red-500 to-pink-500 text-white shadow-lg' 
                  : 'text-gray-400 hover:text-white'
              ]"
            >
              Cards View 🎴
            </button>
            <button 
              @click="viewMode = 'table'"
              :class="[
                'px-6 py-3 rounded-full font-semibold transition-all duration-300',
                viewMode === 'table' 
                  ? 'bg-gradient-to-r from-blue-500 to-cyan-500 text-white shadow-lg' 
                  : 'text-gray-400 hover:text-white'
              ]"
            >
              Table View 📊
            </button>
          </div>

          <!-- Filter Buttons -->
          <div class="flex flex-wrap justify-center gap-4">
            <button class="px-6 py-3 bg-gradient-to-r from-red-500 to-pink-500 text-white font-semibold rounded-full hover:scale-110 transition-all duration-300 hover:shadow-lg hover:shadow-red-500/50">
              All Stars ⭐
            </button>
            <button class="px-6 py-3 bg-gradient-to-r from-blue-500 to-cyan-500 text-white font-semibold rounded-full hover:scale-110 transition-all duration-300 hover:shadow-lg hover:shadow-blue-500/50">
              Developers 👨‍💻
            </button>
            <button class="px-6 py-3 bg-gradient-to-r from-purple-500 to-indigo-500 text-white font-semibold rounded-full hover:scale-110 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/50">
              Designers 🎨
            </button>
            <button class="px-6 py-3 bg-gradient-to-r from-green-500 to-emerald-500 text-white font-semibold rounded-full hover:scale-110 transition-all duration-300 hover:shadow-lg hover:shadow-green-500/50">
              Managers 📊
            </button>
          </div>
        </div>
      </div>

      <!-- Cards View -->
      <div v-if="viewMode === 'cards'" class="max-w-7xl mx-auto grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 mb-16">
        
        <!-- User Card 1 -->
        <div class="group relative">
          <div class="bg-gradient-to-br from-gray-800/60 to-gray-900/60 backdrop-blur-xl rounded-3xl overflow-hidden border border-gray-700/50 hover:border-red-500/80 transition-all duration-500 hover:scale-110 hover:shadow-2xl hover:shadow-red-500/30 hover:-translate-y-4">
            
            <!-- Glow Effect -->
            <div class="absolute inset-0 bg-gradient-to-r from-red-500/10 to-pink-500/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <!-- Profile Image -->
            <div class="relative p-6 pb-4">
              <div class="w-32 h-32 mx-auto bg-gradient-to-br from-red-400 to-pink-600 rounded-full flex items-center justify-center text-6xl shadow-2xl group-hover:animate-bounce relative">
                👨‍💻
                <!-- Online Status -->
                <div class="absolute -bottom-1 -right-1 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-800 flex items-center justify-center animate-pulse">
                  <span class="text-white text-xs">🔥</span>
                </div>
              </div>
              
              <!-- Skill Badges -->
              <div class="flex justify-center space-x-2 mt-4">
                <div class="bg-yellow-500 text-black text-xs px-3 py-1 rounded-full font-bold">React</div>
                <div class="bg-blue-500 text-white text-xs px-3 py-1 rounded-full font-bold">Vue</div>
              </div>
            </div>
            
            <!-- Card Content -->
            <div class="p-6 pt-2 text-center relative z-10">
              <h3 class="text-2xl font-bold bg-gradient-to-r from-red-400 to-pink-400 bg-clip-text text-transparent mb-2">John Doe</h3>
              <p class="text-gray-300 font-semibold mb-2">Frontend Developer 👨‍💻</p>
              <p class="text-gray-400 text-sm mb-4">3+ years experience</p>
              
              <!-- Rating -->
              <div class="flex justify-center items-center mb-4">
                <span class="text-yellow-400 text-lg mr-2">⭐⭐⭐⭐⭐</span>
                <span class="text-yellow-400 font-bold">4.9</span>
              </div>
              
              <!-- Price/Rate -->
              <div class="bg-gradient-to-r from-red-500/20 to-pink-500/20 rounded-2xl p-4 mb-4 border border-red-500/30">
                <p class="text-2xl font-bold text-white">$85<span class="text-sm text-gray-400">/hour</span></p>
                <p class="text-gray-400 text-sm">Available for hire</p>
              </div>
              
              <!-- Action Buttons -->
              <div class="space-y-3">
                <button class="w-full py-3 bg-gradient-to-r from-red-500 to-pink-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-red-500/50">
                  Hire Me! 🚀
                </button>
                <button class="w-full py-3 border-2 border-red-500/50 text-red-400 font-semibold rounded-full hover:bg-red-500/10 hover:scale-105 transition-all duration-300">
                  View Portfolio 👀
                </button>
              </div>
              
              <!-- Social Links -->
              <div class="flex justify-center space-x-4 mt-4">
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
            </div>
          </div>
        </div>

        <!-- User Card 2 -->
        <div class="group relative">
          <div class="bg-gradient-to-br from-gray-800/60 to-gray-900/60 backdrop-blur-xl rounded-3xl overflow-hidden border border-gray-700/50 hover:border-orange-500/80 transition-all duration-500 hover:scale-110 hover:shadow-2xl hover:shadow-orange-500/30 hover:-translate-y-4">
            
            <div class="absolute inset-0 bg-gradient-to-r from-orange-500/10 to-yellow-500/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="relative p-6 pb-4">
              <div class="w-32 h-32 mx-auto bg-gradient-to-br from-orange-400 to-yellow-600 rounded-full flex items-center justify-center text-6xl shadow-2xl group-hover:animate-bounce relative">
                👩‍🎨
                <div class="absolute -bottom-1 -right-1 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-800 flex items-center justify-center animate-pulse">
                  <span class="text-white text-xs">✨</span>
                </div>
              </div>
              
              <div class="flex justify-center space-x-2 mt-4">
                <div class="bg-pink-500 text-white text-xs px-3 py-1 rounded-full font-bold">UI</div>
                <div class="bg-purple-500 text-white text-xs px-3 py-1 rounded-full font-bold">UX</div>
              </div>
            </div>
            
            <div class="p-6 pt-2 text-center relative z-10">
              <h3 class="text-2xl font-bold bg-gradient-to-r from-orange-400 to-yellow-400 bg-clip-text text-transparent mb-2">Jane Smith</h3>
              <p class="text-gray-300 font-semibold mb-2">UI/UX Designer 🎨</p>
              <p class="text-gray-400 text-sm mb-4">5+ years experience</p>
              
              <div class="flex justify-center items-center mb-4">
                <span class="text-yellow-400 text-lg mr-2">⭐⭐⭐⭐⭐</span>
                <span class="text-yellow-400 font-bold">4.8</span>
              </div>
              
              <div class="bg-gradient-to-r from-orange-500/20 to-yellow-500/20 rounded-2xl p-4 mb-4 border border-orange-500/30">
                <p class="text-2xl font-bold text-white">$95<span class="text-sm text-gray-400">/hour</span></p>
                <p class="text-gray-400 text-sm">Design specialist</p>
              </div>
              
              <div class="space-y-3">
                <button class="w-full py-3 bg-gradient-to-r from-orange-500 to-yellow-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-orange-500/50">
                  Let's Design! 🎨
                </button>
                <button class="w-full py-3 border-2 border-orange-500/50 text-orange-400 font-semibold rounded-full hover:bg-orange-500/10 hover:scale-105 transition-all duration-300">
                  See Designs 👁️
                </button>
              </div>
              
              <div class="flex justify-center space-x-4 mt-4">
                <div class="w-10 h-10 bg-pink-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-pink-500/50">
                  <span class="text-white text-sm">🎨</span>
                </div>
                <div class="w-10 h-10 bg-orange-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-orange-500/50">
                  <span class="text-white text-sm">📱</span>
                </div>
                <div class="w-10 h-10 bg-yellow-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-yellow-500/50">
                  <span class="text-white text-sm">💫</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- User Card 3 -->
        <div class="group relative">
          <div class="bg-gradient-to-br from-gray-800/60 to-gray-900/60 backdrop-blur-xl rounded-3xl overflow-hidden border border-gray-700/50 hover:border-green-500/80 transition-all duration-500 hover:scale-110 hover:shadow-2xl hover:shadow-green-500/30 hover:-translate-y-4">
            
            <div class="absolute inset-0 bg-gradient-to-r from-green-500/10 to-emerald-500/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="relative p-6 pb-4">
              <div class="w-32 h-32 mx-auto bg-gradient-to-br from-green-400 to-emerald-600 rounded-full flex items-center justify-center text-6xl shadow-2xl group-hover:animate-bounce relative">
                👨‍🔧
                <div class="absolute -bottom-1 -right-1 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-800 flex items-center justify-center animate-pulse">
                  <span class="text-white text-xs">⚡</span>
                </div>
              </div>
              
              <div class="flex justify-center space-x-2 mt-4">
                <div class="bg-green-500 text-white text-xs px-3 py-1 rounded-full font-bold">Node</div>
                <div class="bg-blue-500 text-white text-xs px-3 py-1 rounded-full font-bold">API</div>
              </div>
            </div>
            
            <div class="p-6 pt-2 text-center relative z-10">
              <h3 class="text-2xl font-bold bg-gradient-to-r from-green-400 to-emerald-400 bg-clip-text text-transparent mb-2">Alex Brown</h3>
              <p class="text-gray-300 font-semibold mb-2">Backend Developer 🔧</p>
              <p class="text-gray-400 text-sm mb-4">4+ years experience</p>
              
              <div class="flex justify-center items-center mb-4">
                <span class="text-yellow-400 text-lg mr-2">⭐⭐⭐⭐⭐</span>
                <span class="text-yellow-400 font-bold">4.7</span>
              </div>
              
              <div class="bg-gradient-to-r from-green-500/20 to-emerald-500/20 rounded-2xl p-4 mb-4 border border-green-500/30">
                <p class="text-2xl font-bold text-white">$75<span class="text-sm text-gray-400">/hour</span></p>
                <p class="text-gray-400 text-sm">API architect</p>
              </div>
              
              <div class="space-y-3">
                <button class="w-full py-3 bg-gradient-to-r from-green-500 to-emerald-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-green-500/50">
                  Build APIs! ⚡
                </button>
                <button class="w-full py-3 border-2 border-green-500/50 text-green-400 font-semibold rounded-full hover:bg-green-500/10 hover:scale-105 transition-all duration-300">
                  View Code 💻
                </button>
              </div>
              
              <div class="flex justify-center space-x-4 mt-4">
                <div class="w-10 h-10 bg-green-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-green-500/50">
                  <span class="text-white text-sm">⚡</span>
                </div>
                <div class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-blue-500/50">
                  <span class="text-white text-sm">🔧</span>
                </div>
                <div class="w-10 h-10 bg-emerald-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-emerald-500/50">
                  <span class="text-white text-sm">🚀</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- User Card 4 -->
        <div class="group relative">
          <div class="bg-gradient-to-br from-gray-800/60 to-gray-900/60 backdrop-blur-xl rounded-3xl overflow-hidden border border-gray-700/50 hover:border-purple-500/80 transition-all duration-500 hover:scale-110 hover:shadow-2xl hover:shadow-purple-500/30 hover:-translate-y-4">
            
            <div class="absolute inset-0 bg-gradient-to-r from-purple-500/10 to-indigo-500/10 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="relative p-6 pb-4">
              <div class="w-32 h-32 mx-auto bg-gradient-to-br from-purple-400 to-indigo-600 rounded-full flex items-center justify-center text-6xl shadow-2xl group-hover:animate-bounce relative">
                👩‍💼
                <div class="absolute -bottom-1 -right-1 w-8 h-8 bg-green-500 rounded-full border-4 border-gray-800 flex items-center justify-center animate-pulse">
                  <span class="text-white text-xs">👑</span>
                </div>
              </div>
              
              <div class="flex justify-center space-x-2 mt-4">
                <div class="bg-purple-500 text-white text-xs px-3 py-1 rounded-full font-bold">PM</div>
                <div class="bg-pink-500 text-white text-xs px-3 py-1 rounded-full font-bold">Lead</div>
              </div>
            </div>
            
            <div class="p-6 pt-2 text-center relative z-10">
              <h3 class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-indigo-400 bg-clip-text text-transparent mb-2">Emily Davis</h3>
              <p class="text-gray-300 font-semibold mb-2">Project Manager 👑</p>
              <p class="text-gray-400 text-sm mb-4">6+ years experience</p>
              
              <div class="flex justify-center items-center mb-4">
                <span class="text-yellow-400 text-lg mr-2">⭐⭐⭐⭐⭐</span>
                <span class="text-yellow-400 font-bold">4.9</span>
              </div>
              
              <div class="bg-gradient-to-r from-purple-500/20 to-indigo-500/20 rounded-2xl p-4 mb-4 border border-purple-500/30">
                <p class="text-2xl font-bold text-white">$120<span class="text-sm text-gray-400">/hour</span></p>
                <p class="text-gray-400 text-sm">Strategy expert</p>
              </div>
              
              <div class="space-y-3">
                <button class="w-full py-3 bg-gradient-to-r from-purple-500 to-indigo-500 text-white font-semibold rounded-full hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/50">
                  Let's Plan! 📋
                </button>
                <button class="w-full py-3 border-2 border-purple-500/50 text-purple-400 font-semibold rounded-full hover:bg-purple-500/10 hover:scale-105 transition-all duration-300">
                  See Results 📊
                </button>
              </div>
              
              <div class="flex justify-center space-x-4 mt-4">
                <div class="w-10 h-10 bg-purple-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-purple-500/50">
                  <span class="text-white text-sm">📊</span>
                </div>
                <div class="w-10 h-10 bg-indigo-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-indigo-500/50">
                  <span class="text-white text-sm">🎯</span>
                </div>
                <div class="w-10 h-10 bg-pink-600 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-pink-500/50">
                  <span class="text-white text-sm">💎</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Table View -->
      <div v-else class="max-w-7xl mx-auto mb-16">
        <div class="bg-gradient-to-br from-gray-800/60 to-gray-900/60 backdrop-blur-xl rounded-3xl border border-gray-700/50 overflow-hidden">
          <!-- Table Header -->
          <div class="bg-gradient-to-r from-red-500/20 via-purple-500/20 to-blue-500/20 p-6 border-b border-gray-700/50">
            <h3 class="text-2xl font-bold bg-gradient-to-r from-red-400 to-blue-400 bg-clip-text text-transparent">
              Team Members Directory 📋
            </h3>
            <p class="text-gray-400 mt-2">Complete overview of our talented team</p>
          </div>

          <!-- Table Content -->
          <div class="overflow-x-auto">
            <table class="w-full">
              <thead>
                <tr class="bg-gradient-to-r from-gray-800/50 to-gray-900/50 border-b border-gray-700/50">
                  <th class="text-left p-6 text-gray-300 font-semibold">Member</th>
                  <th class="text-left p-6 text-gray-300 font-semibold">Role</th>
                  <th class="text-left p-6 text-gray-300 font-semibold">Skills</th>
                  <th class="text-left p-6 text-gray-300 font-semibold">Experience</th>
                  <th class="text-left p-6 text-gray-300 font-semibold">Rating</th>
                  <th class="text-left p-6 text-gray-300 font-semibold">Rate</th>
                  <th class="text-left p-6 text-gray-300 font-semibold">Status</th>
                  <th class="text-left p-6 text-gray-300 font-semibold">Actions</th>
                </tr>
              </thead>
              <tbody>
                <!-- Row 1 -->
                <tr class="border-b border-gray-700/30 hover:bg-gradient-to-r hover:from-red-500/10 hover:to-pink-500/10 transition-all duration-300 group">
                  <td class="p-6">
                    <div class="flex items-center space-x-4">
                      <div class="w-16 h-16 bg-gradient-to-br from-red-400 to-pink-600 rounded-full flex items-center justify-center text-2xl relative">
                        👨‍💻
                        <div class="absolute -bottom-1 -right-1 w-4 h-4 bg-green-500 rounded-full border-2 border-gray-800"></div>
                      </div>
                      <div>
                        <h4 class="text-lg font-bold text-white group-hover:text-red-400 transition-colors">John Doe</h4>
                        <p class="text-gray-400 text-sm">john.doe@email.com</p>
                      </div>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-white font-semibold">Frontend Developer</div>
                    <div class="text-gray-400 text-sm">👨‍💻 Code Wizard</div>
                  </td>
                  <td class="p-6">
                    <div class="flex flex-wrap gap-2">
                      <span class="bg-yellow-500 text-black text-xs px-2 py-1 rounded-full font-bold">React</span>
                      <span class="bg-blue-500 text-white text-xs px-2 py-1 rounded-full font-bold">Vue</span>
                      <span class="bg-green-500 text-white text-xs px-2 py-1 rounded-full font-bold">JS</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-white font-semibold">3+ Years</div>
                    <div class="text-gray-400 text-sm">Since 2021</div>
                  </td>
                  <td class="p-6">
                    <div class="flex items-center">
                      <span class="text-yellow-400 mr-2">⭐⭐⭐⭐⭐</span>
                      <span class="text-yellow-400 font-bold">4.9</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-2xl font-bold text-white">$85</div>
                    <div class="text-gray-400 text-sm">/hour</div>
                  </td>
                  <td class="p-6">
                    <div class="flex items-center">
                      <div class="w-3 h-3 bg-green-500 rounded-full mr-2 animate-pulse"></div>
                      <span class="text-green-400 font-semibold">Available</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="flex space-x-2">
                      <button class="px-4 py-2 bg-gradient-to-r from-red-500 to-pink-500 text-white text-sm font-semibold rounded-full hover:scale-105 transition-all duration-300">
                        Hire 🚀
                      </button>
                      <button class="px-4 py-2 border border-red-500/50 text-red-400 text-sm font-semibold rounded-full hover:bg-red-500/10 transition-all duration-300">
                        View 👀
                      </button>
                    </div>
                  </td>
                </tr>

                <!-- Row 2 -->
                <tr class="border-b border-gray-700/30 hover:bg-gradient-to-r hover:from-orange-500/10 hover:to-yellow-500/10 transition-all duration-300 group">
                  <td class="p-6">
                    <div class="flex items-center space-x-4">
                      <div class="w-16 h-16 bg-gradient-to-br from-orange-400 to-yellow-600 rounded-full flex items-center justify-center text-2xl relative">
                        👩‍🎨
                        <div class="absolute -bottom-1 -right-1 w-4 h-4 bg-green-500 rounded-full border-2 border-gray-800"></div>
                      </div>
                      <div>
                        <h4 class="text-lg font-bold text-white group-hover:text-orange-400 transition-colors">Jane Smith</h4>
                        <p class="text-gray-400 text-sm">jane.smith@email.com</p>
                      </div>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-white font-semibold">UI/UX Designer</div>
                    <div class="text-gray-400 text-sm">🎨 Design Goddess</div>
                  </td>
                  <td class="p-6">
                    <div class="flex flex-wrap gap-2">
                      <span class="bg-pink-500 text-white text-xs px-2 py-1 rounded-full font-bold">UI</span>
                      <span class="bg-purple-500 text-white text-xs px-2 py-1 rounded-full font-bold">UX</span>
                      <span class="bg-orange-500 text-white text-xs px-2 py-1 rounded-full font-bold">Figma</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-white font-semibold">5+ Years</div>
                    <div class="text-gray-400 text-sm">Since 2019</div>
                  </td>
                  <td class="p-6">
                    <div class="flex items-center">
                      <span class="text-yellow-400 mr-2">⭐⭐⭐⭐⭐</span>
                      <span class="text-yellow-400 font-bold">4.8</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-2xl font-bold text-white">$95</div>
                    <div class="text-gray-400 text-sm">/hour</div>
                  </td>
                  <td class="p-6">
                    <div class="flex items-center">
                      <div class="w-3 h-3 bg-green-500 rounded-full mr-2 animate-pulse"></div>
                      <span class="text-green-400 font-semibold">Available</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="flex space-x-2">
                      <button class="px-4 py-2 bg-gradient-to-r from-orange-500 to-yellow-500 text-white text-sm font-semibold rounded-full hover:scale-105 transition-all duration-300">
                        Hire 🎨
                      </button>
                      <button class="px-4 py-2 border border-orange-500/50 text-orange-400 text-sm font-semibold rounded-full hover:bg-orange-500/10 transition-all duration-300">
                        View 👁️
                      </button>
                    </div>
                  </td>
                </tr>

                <!-- Row 3 -->
                <tr class="border-b border-gray-700/30 hover:bg-gradient-to-r hover:from-green-500/10 hover:to-emerald-500/10 transition-all duration-300 group">
                  <td class="p-6">
                    <div class="flex items-center space-x-4">
                      <div class="w-16 h-16 bg-gradient-to-br from-green-400 to-emerald-600 rounded-full flex items-center justify-center text-2xl relative">
                        👨‍🔧
                        <div class="absolute -bottom-1 -right-1 w-4 h-4 bg-green-500 rounded-full border-2 border-gray-800"></div>
                      </div>
                      <div>
                        <h4 class="text-lg font-bold text-white group-hover:text-green-400 transition-colors">Alex Brown</h4>
                        <p class="text-gray-400 text-sm">alex.brown@email.com</p>
                      </div>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-white font-semibold">Backend Developer</div>
                    <div class="text-gray-400 text-sm">🔧 API Architect</div>
                  </td>
                  <td class="p-6">
                    <div class="flex flex-wrap gap-2">
                      <span class="bg-green-500 text-white text-xs px-2 py-1 rounded-full font-bold">Node</span>
                      <span class="bg-blue-500 text-white text-xs px-2 py-1 rounded-full font-bold">API</span>
                      <span class="bg-red-500 text-white text-xs px-2 py-1 rounded-full font-bold">DB</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-white font-semibold">4+ Years</div>
                    <div class="text-gray-400 text-sm">Since 2020</div>
                  </td>
                  <td class="p-6">
                    <div class="flex items-center">
                      <span class="text-yellow-400 mr-2">⭐⭐⭐⭐⭐</span>
                      <span class="text-yellow-400 font-bold">4.7</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-2xl font-bold text-white">$75</div>
                    <div class="text-gray-400 text-sm">/hour</div>
                  </td>
                  <td class="p-6">
                    <div class="flex items-center">
                      <div class="w-3 h-3 bg-green-500 rounded-full mr-2 animate-pulse"></div>
                      <span class="text-green-400 font-semibold">Available</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="flex space-x-2">
                      <button class="px-4 py-2 bg-gradient-to-r from-green-500 to-emerald-500 text-white text-sm font-semibold rounded-full hover:scale-105 transition-all duration-300">
                        Hire ⚡
                      </button>
                      <button class="px-4 py-2 border border-green-500/50 text-green-400 text-sm font-semibold rounded-full hover:bg-green-500/10 transition-all duration-300">
                        View 💻
                      </button>
                    </div>
                  </td>
                </tr>

                <!-- Row 4 -->
                <tr class="hover:bg-gradient-to-r hover:from-purple-500/10 hover:to-indigo-500/10 transition-all duration-300 group">
                  <td class="p-6">
                    <div class="flex items-center space-x-4">
                      <div class="w-16 h-16 bg-gradient-to-br from-purple-400 to-indigo-600 rounded-full flex items-center justify-center text-2xl relative">
                        👩‍💼
                        <div class="absolute -bottom-1 -right-1 w-4 h-4 bg-green-500 rounded-full border-2 border-gray-800"></div>
                      </div>
                      <div>
                        <h4 class="text-lg font-bold text-white group-hover:text-purple-400 transition-colors">Emily Davis</h4>
                        <p class="text-gray-400 text-sm">emily.davis@email.com</p>
                      </div>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-white font-semibold">Project Manager</div>
                    <div class="text-gray-400 text-sm">👑 Strategy Queen</div>
                  </td>
                  <td class="p-6">
                    <div class="flex flex-wrap gap-2">
                      <span class="bg-purple-500 text-white text-xs px-2 py-1 rounded-full font-bold">PM</span>
                      <span class="bg-pink-500 text-white text-xs px-2 py-1 rounded-full font-bold">Lead</span>
                      <span class="bg-indigo-500 text-white text-xs px-2 py-1 rounded-full font-bold">Strategy</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-white font-semibold">6+ Years</div>
                    <div class="text-gray-400 text-sm">Since 2018</div>
                  </td>
                  <td class="p-6">
                    <div class="flex items-center">
                      <span class="text-yellow-400 mr-2">⭐⭐⭐⭐⭐</span>
                      <span class="text-yellow-400 font-bold">4.9</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="text-2xl font-bold text-white">$120</div>
                    <div class="text-gray-400 text-sm">/hour</div>
                  </td>
                  <td class="p-6">
                    <div class="flex items-center">
                      <div class="w-3 h-3 bg-green-500 rounded-full mr-2 animate-pulse"></div>
                      <span class="text-green-400 font-semibold">Available</span>
                    </div>
                  </td>
                  <td class="p-6">
                    <div class="flex space-x-2">
                      <button class="px-4 py-2 bg-gradient-to-r from-purple-500 to-indigo-500 text-white text-sm font-semibold rounded-full hover:scale-105 transition-all duration-300">
                        Hire 📋
                      </button>
                      <button class="px-4 py-2 border border-purple-500/50 text-purple-400 text-sm font-semibold rounded-full hover:bg-purple-500/10 transition-all duration-300">
                        View 📊
                      </button>
                    </div>
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>

      <!-- Bottom CTA Section -->
      <div class="text-center pb-16 max-w-4xl mx-auto">
        <h2 class="text-4xl font-bold bg-gradient-to-r from-red-400 via-purple-500 to-blue-500 bg-clip-text text-transparent mb-6">
          Ready to work with us? ✨
        </h2>
        <p class="text-xl text-gray-400 mb-8">
          Join hundreds of satisfied clients who have transformed their ideas into reality with our amazing team!
        </p>
        
        <div class="flex flex-col sm:flex-row gap-6 justify-center">
          <button class="px-12 py-4 bg-gradient-to-r from-red-500 to-blue-500 text-white font-bold rounded-full hover:scale-110 transition-all duration-300 hover:shadow-2xl hover:shadow-purple-500/50 text-lg">
            Start Your Project 🚀
          </button>
          <button class="px-12 py-4 border-2 border-gray-600 text-white font-bold rounded-full hover:border-purple-500 hover:scale-110 transition-all duration-300 hover:shadow-2xl hover:shadow-purple-500/50 text-lg hover:bg-purple-500/10">
            Schedule a Call 📞
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// Reactive data
const viewMode = ref('cards') // 'cards' or 'table'
</script>

<style scoped>
/* Custom animations */
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-10px); }
}

.animate-float {
  animation: float 3s ease-in-out infinite;
}

/* Gradient border animation */
@keyframes gradient-border {
  0%, 100% { border-color: rgba(239, 68, 68, 0.5); }
  25% { border-color: rgba(168, 85, 247, 0.5); }
  50% { border-color: rgba(59, 130, 246, 0.5); }
  75% { border-color: rgba(34, 197, 94, 0.5); }
}

.group:hover {
  animation: gradient-border 2s ease-in-out infinite;
}

/* Table hover effects */
tbody tr:hover {
  transform: translateX(4px);
}
</style>