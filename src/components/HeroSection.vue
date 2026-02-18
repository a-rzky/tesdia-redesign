<template>
  <section class="relative min-h-screen flex items-center justify-center overflow-hidden pt-20">
    <!-- Background orbs -->
    <div class="orb w-[600px] h-[600px] top-[-200px] left-[-200px]" style="background: #0369a1; animation-delay: 0s;"></div>
    <div class="orb w-[400px] h-[400px] bottom-[-100px] right-[-100px]" style="background: #e8c96e; animation-delay: -3s;"></div>
    <div class="orb w-[300px] h-[300px] top-1/2 right-1/4" style="background: #818cf8; animation-delay: -5s; opacity: 0.08;"></div>

    <!-- Grid overlay -->
    <div class="absolute inset-0 opacity-[0.03]"
      style="background-image: linear-gradient(rgba(255,255,255,0.5) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,0.5) 1px, transparent 1px); background-size: 60px 60px;"></div>

    <div class="relative z-10 max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-16 items-center">
      <!-- Left Content -->
      <div class="space-y-8">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full glass-gold text-xs font-mono text-gold tracking-widest uppercase">
          <span class="w-2 h-2 rounded-full bg-gold animate-pulse"></span>
          Dermatoglyphics Intelligence Analysis
        </div>

        <h1 class="font-display text-5xl lg:text-7xl leading-[1.05] font-bold">
          Kenali
          <span class="text-gradient italic"> Potensi</span>
          <br />Genetikmu
          <br />
          <span class="text-white/30 text-4xl lg:text-5xl font-normal">dari 10 Sidik Jari</span>
        </h1>

        <p class="text-slate-400 text-lg max-w-lg leading-relaxed">
          Teknologi analisis sidik jari paling akurat untuk mengungkap kecerdasan majemuk, karakter, gaya belajar, dan potensi karir Anda — sekali tes, seumur hidup bermanfaat.
        </p>

        <div class="flex flex-wrap gap-4">
          <a href="https://wa.link/6p3kuz" target="_blank"
            class="group flex items-center gap-3 px-8 py-4 rounded-2xl font-semibold text-dark-900 transition-all duration-300 hover:scale-105 hover:shadow-2xl"
            style="background: linear-gradient(135deg, #e8c96e, #f59e0b);">
            Konsultasi Gratis
            <svg class="w-4 h-4 transition-transform group-hover:translate-x-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
            </svg>
          </a>
          <a href="#tentang"
            class="flex items-center gap-2 px-8 py-4 rounded-2xl glass text-white font-medium hover:bg-white/10 transition-all">
            Pelajari Lebih
          </a>
        </div>

        <!-- Stats Row -->
        <div class="flex gap-8 pt-4 border-t border-white/10">
          <div v-for="stat in stats" :key="stat.label">
            <div class="text-2xl font-display font-bold text-gradient">{{ stat.value }}</div>
            <div class="text-xs text-slate-500 mt-0.5">{{ stat.label }}</div>
          </div>
        </div>
      </div>

      <!-- Right: Fingerprint Visual -->
      <div class="relative flex items-center justify-center">
        <div class="relative w-80 h-80 lg:w-[420px] lg:h-[420px]">
          <!-- Outer ring -->
          <div class="absolute inset-0 rounded-full border border-white/10 animate-spin-slow"></div>
          <div class="absolute inset-4 rounded-full border border-brand-500/20 animate-spin-slow" style="animation-direction: reverse; animation-duration: 15s;"></div>
          
          <!-- Center fingerprint card -->
          <div class="absolute inset-10 rounded-full glass flex items-center justify-center animate-float">
            <div class="text-center space-y-2">
              <svg class="w-24 h-24 mx-auto text-brand-400 opacity-80" viewBox="0 0 100 100" fill="none" stroke="currentColor" stroke-width="1.5">
                <path d="M50 10 C28 10, 10 28, 10 50 C10 72, 28 90, 50 90 C72 90, 90 72, 90 50" stroke-linecap="round"/>
                <path d="M50 20 C33 20, 20 33, 20 50 C20 67, 33 80, 50 80 C67 80, 80 67, 80 50" stroke-linecap="round"/>
                <path d="M50 30 C38 30, 30 38, 30 50 C30 62, 38 70, 50 70 C62 70, 70 62, 70 50" stroke-linecap="round"/>
                <path d="M50 40 C44 40, 40 44, 40 50 C40 56, 44 60, 50 60 C56 60, 60 56, 60 50" stroke-linecap="round"/>
                <circle cx="50" cy="50" r="4" fill="currentColor" opacity="0.6"/>
                <path d="M15 35 Q20 25, 30 20" stroke-linecap="round"/>
                <path d="M85 35 Q80 25, 70 20" stroke-linecap="round"/>
              </svg>
              <p class="text-xs font-mono text-brand-400/70 tracking-widest">SCANNING...</p>
            </div>
          </div>

          <!-- Floating badges -->
          <div v-for="badge in floatingBadges" :key="badge.label"
            class="absolute glass-gold rounded-2xl px-3 py-2 text-xs font-medium text-gold animate-float"
            :style="badge.style">
            <div class="flex items-center gap-1.5">
              <span class="text-base">{{ badge.icon }}</span>
              {{ badge.label }}
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Scroll indicator -->
    <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 text-slate-600">
      <span class="text-xs font-mono tracking-widest">SCROLL</span>
      <div class="w-px h-12 bg-gradient-to-b from-slate-600 to-transparent"></div>
    </div>
  </section>
</template>

<script setup>
const stats = [
  { value: '5000+', label: 'Peserta' },
  { value: '85%+', label: 'Akurasi' },
  { value: '1×', label: 'Seumur Hidup' },
]
const floatingBadges = [
  { icon: '🧬', label: 'Genetik', style: 'top: 5%; left: 0%; animation-delay: -1s;' },
  { icon: '🧠', label: 'Kecerdasan', style: 'top: 20%; right: -5%; animation-delay: -2s;' },
  { icon: '🎯', label: 'Karir', style: 'bottom: 20%; right: -5%; animation-delay: -3s;' },
  { icon: '📚', label: 'Gaya Belajar', style: 'bottom: 5%; left: 5%; animation-delay: -4s;' },
]
</script>
