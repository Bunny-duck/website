<template>
  <div class="min-h-screen bg-gradient-to-br from-gray-900 via-purple-900 to-gray-900 relative overflow-hidden">
    <!-- Animated Background Elements -->
    <div class="absolute inset-0 overflow-hidden">
      <div class="absolute top-20 left-20 w-96 h-96 bg-gradient-to-r from-red-500/10 to-pink-500/10 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute bottom-20 right-20 w-80 h-80 bg-gradient-to-r from-blue-500/10 to-cyan-500/10 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute top-1/2 left-1/4 w-64 h-64 bg-gradient-to-r from-purple-500/5 to-indigo-500/5 rounded-full blur-3xl animate-pulse"></div>
    </div>

    <div class="relative z-10 flex items-center justify-center min-h-screen p-6">
      <div class="flex bg-gradient-to-br from-gray-800/60 to-gray-900/60 backdrop-blur-xl rounded-3xl shadow-2xl overflow-hidden border border-gray-700/50 max-w-6xl w-full" style="min-height: 600px;">
        
        <!-- Form Section -->
        <div class="w-full lg:w-1/2 p-12 flex flex-col justify-center relative">
          <!-- Glow Effect -->
          <div class="absolute inset-0 bg-gradient-to-r from-red-500/5 to-blue-500/5 rounded-l-3xl"></div>
          
          <div class="relative z-10">
            <div class="mb-8">
              <h2 class="text-5xl font-extrabold bg-gradient-to-r from-red-400 via-purple-500 to-blue-500 bg-clip-text text-transparent mb-4">
                Let's Connect! 👋
              </h2>
              <p class="text-xl text-gray-300 leading-relaxed">
                Ready to bring your ideas to life? Drop us a message and let's create something 
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-red-400 to-blue-400 font-semibold">amazing together!</span> ✨
              </p>
            </div>

            <!-- Social Login Button -->
            <button class="flex items-center justify-center w-full bg-gradient-to-r from-gray-700/50 to-gray-800/50 backdrop-blur-lg text-white py-4 rounded-2xl mb-6 hover:scale-105 transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/25 border border-gray-600/50">
              <span class="mr-3 text-2xl">🍏</span> 
              <span class="font-semibold">Continue with Apple</span>
            </button>

            <!-- Divider -->
            <div class="flex items-center mb-6">
              <div class="flex-1 h-px bg-gradient-to-r from-transparent via-gray-600 to-transparent"></div>
              <span class="px-4 text-gray-400 font-medium">or send us a message</span>
              <div class="flex-1 h-px bg-gradient-to-r from-transparent via-gray-600 to-transparent"></div>
            </div>

            <!-- Contact Form -->
            <form @submit.prevent="handleSubmit" class="space-y-6">
              <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="relative group">
                  <input 
                    v-model="form.firstName"
                    type="text" 
                    placeholder="First Name" 
                    class="w-full p-4 bg-gray-800/50 backdrop-blur-lg border border-gray-600/50 rounded-2xl focus:outline-none focus:ring-2 focus:ring-red-500/50 focus:border-red-500/50 text-white placeholder-gray-400 transition-all duration-300 group-hover:border-purple-500/50"
                    required
                  >
                  <div class="absolute inset-0 bg-gradient-to-r from-red-500/10 to-pink-500/10 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none"></div>
                </div>
                
                <div class="relative group">
                  <input 
                    v-model="form.lastName"
                    type="text" 
                    placeholder="Last Name" 
                    class="w-full p-4 bg-gray-800/50 backdrop-blur-lg border border-gray-600/50 rounded-2xl focus:outline-none focus:ring-2 focus:ring-blue-500/50 focus:border-blue-500/50 text-white placeholder-gray-400 transition-all duration-300 group-hover:border-purple-500/50"
                    required
                  >
                  <div class="absolute inset-0 bg-gradient-to-r from-blue-500/10 to-cyan-500/10 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none"></div>
                </div>
              </div>

              <div class="relative group">
                <input 
                  v-model="form.email"
                  type="email" 
                  placeholder="Email Address" 
                  class="w-full p-4 bg-gray-800/50 backdrop-blur-lg border border-gray-600/50 rounded-2xl focus:outline-none focus:ring-2 focus:ring-purple-500/50 focus:border-purple-500/50 text-white placeholder-gray-400 transition-all duration-300 group-hover:border-purple-500/50"
                  required
                >
                <div class="absolute inset-0 bg-gradient-to-r from-purple-500/10 to-indigo-500/10 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none"></div>
              </div>

              <div class="relative group">
                <input 
                  v-model="form.subject"
                  type="text" 
                  placeholder="Subject" 
                  class="w-full p-4 bg-gray-800/50 backdrop-blur-lg border border-gray-600/50 rounded-2xl focus:outline-none focus:ring-2 focus:ring-green-500/50 focus:border-green-500/50 text-white placeholder-gray-400 transition-all duration-300 group-hover:border-purple-500/50"
                  required
                >
                <div class="absolute inset-0 bg-gradient-to-r from-green-500/10 to-emerald-500/10 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none"></div>
              </div>

              <div class="relative group">
                <textarea 
                  v-model="form.message"
                  placeholder="Tell us about your project..." 
                  rows="4"
                  class="w-full p-4 bg-gray-800/50 backdrop-blur-lg border border-gray-600/50 rounded-2xl focus:outline-none focus:ring-2 focus:ring-yellow-500/50 focus:border-yellow-500/50 text-white placeholder-gray-400 transition-all duration-300 group-hover:border-purple-500/50 resize-none"
                  required
                ></textarea>
                <div class="absolute inset-0 bg-gradient-to-r from-yellow-500/10 to-orange-500/10 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300 pointer-events-none"></div>
              </div>

              <div class="flex items-center justify-between text-sm">
                <label class="flex items-center text-gray-300 cursor-pointer group">
                  <input 
                    v-model="form.newsletter"
                    type="checkbox" 
                    class="mr-3 w-4 h-4 text-purple-500 bg-gray-800 border-gray-600 rounded focus:ring-purple-500 focus:ring-2"
                  > 
                  <span class="group-hover:text-purple-400 transition-colors">Subscribe to our newsletter 📧</span>
                </label>
                <a href="#" class="text-blue-400 hover:text-blue-300 transition-colors hover:underline">Privacy Policy</a>
              </div>

              <button 
                type="submit" 
                :disabled="isSubmitting"
                class="w-full bg-gradient-to-r from-red-500 via-purple-500 to-blue-500 text-white py-4 rounded-2xl font-bold text-lg hover:scale-105 transition-all duration-300 hover:shadow-2xl hover:shadow-purple-500/50 disabled:opacity-50 disabled:cursor-not-allowed relative overflow-hidden group"
              >
                <span v-if="!isSubmitting" class="relative z-10">Send Message 🚀</span>
                <span v-else class="relative z-10">Sending... ⏳</span>
                <div class="absolute inset-0 bg-gradient-to-r from-blue-500 via-purple-500 to-red-500 opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
              </button>

              <p class="text-center text-gray-400 mt-6">
                Prefer email? Reach us at 
                <a href="mailto:hello@company.com" class="text-purple-400 hover:text-purple-300 transition-colors hover:underline font-semibold">
                  hello@company.com
                </a> 💌
              </p>
            </form>
          </div>
        </div>

        <!-- Info Section -->
        <div class="hidden lg:flex lg:w-1/2 bg-gradient-to-br from-purple-600/20 to-blue-600/20 backdrop-blur-lg relative overflow-hidden">
          <!-- Background Pattern -->
          <div class="absolute inset-0 opacity-10">
            <div class="absolute top-10 left-10 w-32 h-32 border-2 border-white rounded-full"></div>
            <div class="absolute top-32 right-20 w-24 h-24 border-2 border-white rounded-full"></div>
            <div class="absolute bottom-20 left-20 w-40 h-40 border-2 border-white rounded-full"></div>
            <div class="absolute bottom-32 right-10 w-20 h-20 border-2 border-white rounded-full"></div>
          </div>

          <div class="relative z-10 p-12 flex flex-col justify-center text-white">
            <div class="mb-12">
              <h3 class="text-4xl font-bold mb-6 bg-gradient-to-r from-white to-gray-300 bg-clip-text text-transparent">
                Get in Touch ✨
              </h3>
              <p class="text-xl text-gray-300 leading-relaxed mb-8">
                We're here to help bring your vision to life. Whether it's a quick question or a big project, 
                we'd love to hear from you!
              </p>
            </div>

            <!-- Contact Info Cards -->
            <div class="space-y-6">
              <div class="bg-white/10 backdrop-blur-lg rounded-2xl p-6 border border-white/20 hover:bg-white/20 transition-all duration-300 group cursor-pointer">
                <div class="flex items-center">
                  <div class="w-12 h-12 bg-gradient-to-r from-red-500 to-pink-500 rounded-full flex items-center justify-center text-2xl mr-4 group-hover:scale-110 transition-transform">
                    📧
                  </div>
                  <div>
                    <h4 class="font-semibold text-lg">Email Us</h4>
                    <p class="text-gray-300">bunny@gmail.com</p>
                  </div>
                </div>
              </div>

              <div class="bg-white/10 backdrop-blur-lg rounded-2xl p-6 border border-white/20 hover:bg-white/20 transition-all duration-300 group cursor-pointer">
                <div class="flex items-center">
                  <div class="w-12 h-12 bg-gradient-to-r from-blue-500 to-cyan-500 rounded-full flex items-center justify-center text-2xl mr-4 group-hover:scale-110 transition-transform">
                    📱
                  </div>
                  <div>
                    <h4 class="font-semibold text-lg">Call Us</h4>
                    <p class="text-gray-300">+1 (555) 123-4567</p>
                  </div>
                </div>
              </div>

              <div class="bg-white/10 backdrop-blur-lg rounded-2xl p-6 border border-white/20 hover:bg-white/20 transition-all duration-300 group cursor-pointer">
                <div class="flex items-center">
                  <div class="w-12 h-12 bg-gradient-to-r from-green-500 to-emerald-500 rounded-full flex items-center justify-center text-2xl mr-4 group-hover:scale-110 transition-transform">
                    📍
                  </div>
                  <div>
                    <h4 class="font-semibold text-lg">Visit Us</h4>
                    <p class="text-gray-300">BP 511, Phum Tropeang Chhuk Sangtak, Street 371</p>
                  </div>
                </div>
              </div>
            </div>

            <!-- Social Links -->
            <div class="mt-12">
              <h4 class="text-lg font-semibold mb-4">Follow Us</h4>
              <div class="flex space-x-4">
                <div class="w-12 h-12 bg-gradient-to-r from-purple-500 to-indigo-500 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-purple-500/50">
                  <span class="text-white text-lg">🐙</span>
                </div>
                <div class="w-12 h-12 bg-gradient-to-r from-blue-500 to-cyan-500 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-blue-500/50">
                  <span class="text-white text-lg">💼</span>
                </div>
                <div class="w-12 h-12 bg-gradient-to-r from-pink-500 to-red-500 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-pink-500/50">
                  <span class="text-white text-lg">📱</span>
                </div>
                <div class="w-12 h-12 bg-gradient-to-r from-green-500 to-emerald-500 rounded-full flex items-center justify-center hover:scale-125 transition-transform cursor-pointer hover:shadow-lg hover:shadow-green-500/50">
                  <span class="text-white text-lg">🎵</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Success Message -->
    <div 
      v-if="showSuccess" 
      class="fixed top-8 right-8 bg-gradient-to-r from-green-500 to-emerald-500 text-white px-6 py-4 rounded-2xl shadow-2xl z-50 transform transition-all duration-500"
      :class="showSuccess ? 'translate-x-0 opacity-100' : 'translate-x-full opacity-0'"
    >
      <div class="flex items-center">
        <span class="text-2xl mr-3">✅</span>
        <div>
          <h4 class="font-bold">Message Sent!</h4>
          <p class="text-sm">We'll get back to you soon.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue'

// Form data
const form = reactive({
  firstName: '',
  lastName: '',
  email: '',
  subject: '',
  message: '',
  newsletter: false
})

// Form state
const isSubmitting = ref(false)
const showSuccess = ref(false)

// Handle form submission
const handleSubmit = async () => {
  isSubmitting.value = true
  
  // Simulate API call
  await new Promise(resolve => setTimeout(resolve, 2000))
  
  // Reset form
  Object.keys(form).forEach(key => {
    if (typeof form[key] === 'boolean') {
      form[key] = false
    } else {
      form[key] = ''
    }
  })
  
  isSubmitting.value = false
  showSuccess.value = true
  
  // Hide success message after 5 seconds
  setTimeout(() => {
    showSuccess.value = false
  }, 5000)
}
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

/* Input focus effects */
input:focus, textarea:focus {
  transform: translateY(-2px);
}

/* Button hover effects */
button:hover:not(:disabled) {
  transform: translateY(-2px);
}

/* Gradient border animation */
@keyframes gradient-border {
  0%, 100% { border-color: rgba(239, 68, 68, 0.5); }
  25% { border-color: rgba(168, 85, 247, 0.5); }
  50% { border-color: rgba(59, 130, 246, 0.5); }
  75% { border-color: rgba(34, 197, 94, 0.5); }
}

.group:hover input, .group:hover textarea {
  animation: gradient-border 2s ease-in-out infinite;
}
</style>