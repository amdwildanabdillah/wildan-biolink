<script setup>
import { ref } from 'vue'
import Footer from './components/Footer.vue'
import { 
  ArrowUpRightIcon,
  ArrowDownTrayIcon 
} from '@heroicons/vue/24/solid'

import { 
  PhPlant, 
  PhInstagramLogo,
  PhFileText, // <--- Icon Dokumen Pricelist
  PhTag       // <--- Opsi lain: Icon Label Harga
} from '@phosphor-icons/vue'

// --- DATA LINKS (SESUAI REQUEST: lp.png, vixel.png, desto.png) ---
const mainLinks = [
  { 
    id: 1,
    name: 'Personal Portfolio', 
    desc: 'Fullstack Creative Resume',
    url: 'https://portfoliowildan.my.id', 
    type: 'web',
    image: '/lp.png', // FILE TETAP INI
    colorClass: 'group-hover:border-indigo-500 group-hover:shadow-[0_0_20px_rgba(99,102,241,0.3)]',
    textClass: 'group-hover:text-indigo-400'
  },
  { 
    id: 2,
    name: 'Vixel Creative', 
    desc: 'Digital Studio Based in Surabaya',
    url: 'https://vixelcreative.my.id', 
    type: 'web',
    image: '/vixel.png', // FILE TETAP INI
    colorClass: 'group-hover:border-cyan-500 group-hover:shadow-[0_0_20px_rgba(6,182,212,0.3)]',
    textClass: 'group-hover:text-cyan-400'
  },
  { 
    id: 3,
    name: 'Storydesto', 
    desc: 'Capture Your Best Moment',
    url: 'https://portfolio-storydesto.netlify.app',
    type: 'web',
    image: '/desto.png', // FILE TETAP INI
    colorClass: 'group-hover:border-amber-500 group-hover:shadow-[0_0_20px_rgba(245,158,11,0.3)]',
    textClass: 'group-hover:text-amber-400'
  },
]

// --- RESOURCES & SOSMED ---
const secondaryLinks = [
  { 
    id: 5,
    name: 'Instagram Storydesto', 
    desc: 'Create Story with Us',
    url: 'https://instagram.com/storydesto', 
    type: 'social',
    icon: PhInstagramLogo, 
    iconBg: 'bg-pink-900/40 text-pink-400',
    colorClass: 'group-hover:border-pink-500 group-hover:shadow-[0_0_20px_rgba(236,72,153,0.3)]',
    textClass: 'group-hover:text-pink-400'
  },
  {
    id: 6,
    name: 'Instagram Destograph', 
    desc: 'Visual Branding & Production',
    url: 'https://instagram.com/destograph_', 
    type: 'social',
    icon: PhInstagramLogo, 
    iconBg: 'bg-pink-900/40 text-pink-400',
    colorClass: 'group-hover:border-pink-500 group-hover:shadow-[0_0_20px_rgba(236,72,153,0.3)]',
    textClass: 'group-hover:text-pink-400'
  },
  { 
    id: 7,
    name: 'Storydesto Pricelist', 
    desc: 'Download Graduation Package 2026', 
    url: '/pricelist-storydesto.pdf', 
    type: 'download', 
    
    // --- UPDATE DI SINI ---
    image: null, // Logo dimatikan biar gak dobel
    icon: PhFileText, // Ganti jadi Icon File (Dokumen)
    iconBg: 'bg-amber-900/40 text-amber-400', // Background Emas Transparan
    
    colorClass: 'group-hover:border-amber-500 group-hover:shadow-[0_0_20px_rgba(245,158,11,0.3)]',
    textClass: 'group-hover:text-amber-400'
  },
]
</script>

<template>
  <main class="min-h-screen relative flex flex-col font-sans bg-[#030303] text-white overflow-x-hidden selection:bg-cyan-500/30">
    
    <div class="fixed top-[-10%] left-1/2 -translate-x-1/2 w-[300px] h-[300px] bg-cyan-500/20 rounded-full blur-[90px] pointer-events-none z-0"></div>

    <div class="flex-grow flex flex-col items-center px-4 pt-20 z-10 w-full max-w-lg mx-auto">
      
     <div class="text-center mb-10 space-y-4 animate-fade-in-down">
        
        <h1 class="text-4xl sm:text-5xl font-extrabold tracking-tight leading-tight">
          <span class="block text-transparent bg-clip-text bg-gradient-to-r from-white to-cyan-200">
            Visuals by Heart.
          </span>
          <span class="block text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 to-blue-500">
            Logic by Code.
          </span>
        </h1>

        <div class="relative w-28 h-28 mx-auto mt-8 mb-4">
          <div class="absolute -inset-3 bg-cyan-500/20 rounded-full blur-xl animate-pulse"></div>
          
          <div class="relative w-full h-full rounded-full p-1 bg-gradient-to-b from-white/10 to-transparent border border-white/10 shadow-2xl">
             <img 
              src="/foto.jpg" 
              alt="Ahmad Wildan Abdillah" 
              class="w-full h-full object-cover rounded-full"
            />
          </div>
          
          <div class="absolute bottom-0 right-0 bg-[#030303] border border-cyan-500/50 rounded-full p-1.5">
            <div class="w-2.5 h-2.5 bg-cyan-400 rounded-full animate-ping"></div>
            <div class="absolute top-1.5 left-1.5 w-2.5 h-2.5 bg-cyan-400 rounded-full"></div>
          </div>
        </div>

        <div class="space-y-1">
          <h2 class="text-white font-bold text-lg tracking-wide">
            Ahmad Wildan Abdillah
          </h2>
          <p class="text-cyan-400/80 text-[10px] font-bold uppercase tracking-[0.2em]">
            Fullstack Creative
          </p>
          <p class="text-gray-500 text-xs font-medium pt-2 max-w-xs mx-auto leading-relaxed">
            Building digital products with code & capturing moments with lens.
          </p>
        </div>

      </div>

       <div class="w-full flex items-center gap-4 mb-6 px-2 opacity-40">
        <div class="h-[1px] bg-white/30 flex-1"></div>
        <span class="text-[10px] uppercase tracking-widest font-bold text-gray-400">My Ventures Websites</span>
        <div class="h-[1px] bg-white/30 flex-1"></div>
      </div>

      <div class="w-full flex flex-col gap-4 mb-8">
        <a 
          v-for="link in mainLinks" 
          :key="link.id"
          :href="link.url"
          target="_blank"
          class="group relative flex items-center gap-4 p-2 pr-4 bg-white/5 border border-white/10 rounded-full transition-all duration-300 hover:-translate-y-1 hover:bg-white/10 backdrop-blur-sm"
          :class="link.colorClass"
        >
          <div class="w-14 h-14 flex-shrink-0 rounded-full overflow-hidden border border-white/10 ml-0.5 flex items-center justify-center"
               :class="link.image ? 'p-0.5 bg-black/50' : link.iconBg">
            
            <img v-if="link.image" :src="link.image" class="w-full h-full object-cover rounded-full" />
            <component v-else :is="link.icon" class="w-7 h-7" weight="duotone" />
          </div>

          <div class="flex-1 min-w-0 py-2">
            <h3 class="font-bold text-base truncate text-white transition-colors leading-snug" :class="link.textClass">
              {{ link.name }}
            </h3>
            <p class="text-xs text-gray-400 truncate leading-snug">{{ link.desc }}</p>
          </div>

          <div class="w-8 h-8 flex items-center justify-center rounded-full bg-white/5 text-gray-400 group-hover:bg-white/20 group-hover:text-white transition flex-shrink-0">
            <ArrowUpRightIcon class="w-4 h-4" />
          </div>
        </a>
      </div>

      <div class="w-full flex items-center gap-4 mb-6 px-2 opacity-40">
        <div class="h-[1px] bg-white/30 flex-1"></div>
        <span class="text-[10px] uppercase tracking-widest font-bold text-gray-400">Resources & Socials</span>
        <div class="h-[1px] bg-white/30 flex-1"></div>
      </div>

      <div class="w-full flex flex-col gap-4">
        <a 
          v-for="link in secondaryLinks" 
          :key="link.id"
          :href="link.url"
          :download="link.type === 'download' ? '' : null" 
          :target="link.type === 'download' ? '_self' : '_blank'"
          class="group relative flex items-center gap-4 p-2 pr-4 bg-white/5 border border-white/10 rounded-full transition-all duration-300 hover:-translate-y-1 hover:bg-white/10 backdrop-blur-sm"
          :class="link.colorClass"
        >
          <div class="w-14 h-14 flex-shrink-0 rounded-full overflow-hidden border border-white/10 ml-0.5 flex items-center justify-center"
               :class="link.image ? 'p-0.5 bg-black/50' : link.iconBg">
            <img v-if="link.image" :src="link.image" class="w-full h-full object-cover rounded-full" />
            <component v-else :is="link.icon" class="w-7 h-7" weight="duotone" />
          </div>

          <div class="flex-1 min-w-0 py-2">
            <h3 class="font-bold text-base truncate text-white transition-colors leading-snug" :class="link.textClass">
              {{ link.name }}
            </h3>
            <p class="text-xs text-gray-400 truncate leading-snug">{{ link.desc }}</p>
          </div>

          <div class="w-8 h-8 flex items-center justify-center rounded-full bg-white/5 text-gray-400 group-hover:bg-white/20 group-hover:text-white transition flex-shrink-0">
            <ArrowDownTrayIcon v-if="link.type === 'download'" class="w-4 h-4" />
            <ArrowUpRightIcon v-else class="w-4 h-4" />
          </div>
        </a>
      </div>

    </div>

    <Footer />

    <a 
      href="https://wa.me/6285232351908?text=Halo%20Raden%20Mas%20Wildan,%20saya%20tertarik%20untuk%20diskusi%20project." 
      target="_blank"
      class="fixed bottom-6 right-6 z-50 w-14 h-14 flex items-center justify-center bg-[#25D366] hover:bg-[#20bd5a] rounded-full shadow-2xl animate-bounce-slow transition hover:scale-110"
    >
      <svg viewBox="0 0 24 24" class="w-8 h-8 fill-white" xmlns="http://www.w3.org/2000/svg">
        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
      </svg>
    </a>

  </main>
</template>

<style scoped>
.animate-fade-in-down {
  animation: fadeInDown 1s ease-out;
}
@keyframes fadeInDown {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-bounce-slow {
  animation: bounceSlow 3s infinite;
}
@keyframes bounceSlow {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}
</style>