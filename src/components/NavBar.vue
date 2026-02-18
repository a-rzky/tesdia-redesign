<template>
  <nav
    class="fixed top-0 left-0 right-0 z-50 transition-all duration-500"
    :class="scrolled ? 'glass border-b border-white/5 py-3' : 'py-5'"
  >
    <div class="max-w-7xl mx-auto px-6 flex items-center justify-between">
      <!-- Logo -->
      <a href="#" class="flex items-center gap-3">
        <div class="w-9 h-9 rounded-xl flex items-center justify-center" style="background: linear-gradient(135deg, #e8c96e, #0ea5e9);">
          <span class="text-dark-900 font-mono font-bold text-sm">DIA</span>
        </div>
        <span class="font-display text-xl text-white font-semibold">Tes<span class="text-gradient">DIA</span></span>
      </a>

      <!-- Desktop Nav -->
      <div class="hidden md:flex items-center gap-8">
        <a v-for="item in navItems" :key="item.label" :href="item.href"
          class="text-sm text-slate-400 hover:text-white transition-colors duration-200 font-medium">
          {{ item.label }}
        </a>
      </div>

      <!-- CTA -->
      <div class="flex items-center gap-3">
        <a href="https://apps2.tesdia.id/" target="_blank"
          class="hidden md:block text-sm text-slate-300 hover:text-white transition-colors">Masuk</a>
        <a href="https://wa.link/6p3kuz" target="_blank"
          class="px-5 py-2.5 rounded-full text-sm font-semibold transition-all duration-300 hover:scale-105 hover:shadow-lg"
          style="background: linear-gradient(135deg, #e8c96e, #f59e0b); color: #0d1628;">
          Mulai Tes →
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted } from 'vue'
const scrolled = ref(false)
const navItems = [
  { label: 'Tentang DIA', href: '#tentang' },
  { label: 'Manfaat', href: '#manfaat' },
  { label: 'Harga', href: '#harga' },
  { label: 'Testimoni', href: '#testimoni' },
  { label: 'FAQ', href: '#faq' },
  { label: 'Konsultan', href: '#konsultan' },
]
onMounted(() => {
  window.addEventListener('scroll', () => {
    scrolled.value = window.scrollY > 50
  })
})
</script>
