<script setup>
import { 
  PhInstagramLogo, 
  PhLinkedinLogo, 
  PhGithubLogo, 
  PhBehanceLogo, 
  PhYoutubeLogo, 
  PhEnvelopeSimple 
} from '@phosphor-icons/vue'

const socialLinks = [
  {
    name: 'Instagram',
    url: 'https://instagram.com/vixelcreative',
    icon: PhInstagramLogo,
    class: 'hover:bg-[#E1306C]/10 hover:border-[#E1306C] group-hover:text-[#E1306C]',
  },
  {
    name: 'LinkedIn',
    url: 'https://www.linkedin.com/in/ahmadwildanabdillah-vixel',
    icon: PhLinkedinLogo,
    class: 'hover:bg-[#0077b5]/10 hover:border-[#0077b5] group-hover:text-[#0077b5]',
  },
  {
    name: 'GitHub',
    url: 'https://github.com/amdwildanabdillah',
    icon: PhGithubLogo,
    class: 'hover:bg-white/10 hover:border-white group-hover:text-white',
  },
  {
    name: 'Behance',
    url: 'https://behance.net/idan_abdll',
    icon: PhBehanceLogo,
    class: 'hover:bg-[#1769ff]/10 hover:border-[#1769ff] group-hover:text-[#1769ff]',
  },
  {
    name: 'YouTube',
    url: 'https://www.youtube.com/@idan_abdll',
    icon: PhYoutubeLogo,
    class: 'hover:bg-[#ff0000]/10 hover:border-[#ff0000] group-hover:text-[#ff0000]',
  },
  {
    name: 'Email Us',
    url: 'mailto:vixelcreative.id@gmail.com',
    icon: PhEnvelopeSimple,
    class: 'hover:bg-orange-500/10 hover:border-orange-500 group-hover:text-orange-500',
  }
]

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' })
}
</script>

<template>
  <footer class="bg-[#050505] border-t border-white/5 pt-12 pb-24 relative z-0 mt-20 w-full">
    <div class="max-w-lg mx-auto px-6 w-full">
      <div class="grid grid-cols-1 gap-10">
        
        <div class="space-y-4">
          <div @click="scrollToTop" class="cursor-pointer inline-block">
            <span class="font-extrabold text-xl tracking-tighter uppercase text-white">
              VIXEL CREATIVE<span class="text-cyan-400">.</span>
            </span>
          </div>
          <p class="text-gray-400 text-xs leading-loose">
            Studio digital berbasis di Surabaya yang menjembatani logika bisnis (Code) dengan estetika visual (Art).
          </p>
          
          <div class="pt-2">
             <span class="text-cyan-400 text-[10px] font-bold uppercase tracking-widest mb-3 block">
               Initiated By
             </span>
             <a href="https://portfoliowildan.my.id" target="_blank" class="flex items-center gap-3 group w-fit bg-white/5 pr-5 p-1 rounded-full border border-white/10 hover:border-cyan-400 transition">
                <img src="/wildan.jpg" class="w-8 h-8 rounded-full border border-white/10 object-cover" />
                <div>
                  <p class="font-bold text-white text-xs group-hover:text-cyan-400 transition">Ahmad Wildan Abdillah</p>
                </div>
             </a>
          </div>
        </div>

        <div>
          <span class="text-gray-500 text-[10px] font-bold uppercase tracking-widest block mb-4">
            Connect with Us
          </span>
          <div class="grid grid-cols-2 gap-3">
            <a 
              v-for="social in socialLinks"
              :key="social.name"
              :href="social.url"
              target="_blank"
              class="flex items-center gap-3 p-3 rounded-xl border border-white/10 bg-white/5 transition duration-300 group"
              :class="social.class"
            >
              <component 
                :is="social.icon" 
                class="text-xl text-gray-400 transition duration-300 group-hover:text-inherit" 
                weight="regular"
              />
              <span class="font-bold text-xs text-gray-300 group-hover:text-white transition duration-300">
                {{ social.name }}
              </span>
            </a>
          </div>
        </div>
      </div>

      <div class="mt-10 pt-6 border-t border-white/5 text-center">
         <p class="text-[10px] text-gray-600 uppercase tracking-widest font-bold">
           &copy; 2026 Vixel Creative. Surabaya, Indonesia.
         </p>
      </div>
    </div>
  </footer>
</template>