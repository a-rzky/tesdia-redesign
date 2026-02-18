<template>
  <section id="manfaat" class="py-32 relative overflow-hidden">
    <!-- bg accent -->
    <div class="absolute inset-0 opacity-30" style="background: radial-gradient(ellipse at 70% 50%, rgba(232, 201, 110, 0.05) 0%, transparent 70%);"></div>

    <div class="max-w-7xl mx-auto px-6">
      <div class="text-center mb-20 reveal">
        <span class="font-mono text-xs text-gold tracking-[0.3em] uppercase">Manfaat</span>
        <h2 class="mt-4 font-display text-4xl lg:text-6xl font-bold">
          Untuk Siapa<br />
          <span class="text-gradient-blue italic">Tes DIA?</span>
        </h2>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-4">
        <div v-for="(group, i) in groups" :key="i"
          class="reveal glass rounded-3xl p-7 hover:scale-105 transition-all duration-500 group cursor-default"
          :style="{ transitionDelay: i * 100 + 'ms' }">
          <div class="text-5xl mb-5">{{ group.icon }}</div>
          <h3 class="font-display text-xl font-semibold text-white mb-3">{{ group.title }}</h3>
          <ul class="space-y-2">
            <li v-for="benefit in group.benefits" :key="benefit" class="flex items-start gap-2 text-sm text-slate-400">
              <span class="text-brand-400 mt-0.5 flex-shrink-0">✦</span>
              {{ benefit }}
            </li>
          </ul>
        </div>
      </div>

      <!-- CTA Banner -->
      <div class="mt-16 reveal glass rounded-3xl p-10 lg:p-14 relative overflow-hidden" style="background: linear-gradient(135deg, rgba(14,165,233,0.12), rgba(232,201,110,0.08));">
        <div class="orb w-80 h-80 -right-20 -top-20" style="background: #e8c96e; filter: blur(100px); opacity: 0.1; animation: none;"></div>
        <div class="relative z-10 lg:flex items-center justify-between gap-8">
          <div>
            <h3 class="font-display text-3xl lg:text-4xl font-bold">
              Bayangkan jika Anda tahu<br />
              <span class="text-gradient italic">kekuatan sejati Anda</span> lebih awal.
            </h3>
            <p class="text-slate-400 mt-4 max-w-xl">Ribuan orang sudah membuktikannya. Hemat waktu, hemat energi dari trial & error. Mulai dengan tes sidik jari hari ini.</p>
          </div>
          <div class="mt-8 lg:mt-0 flex-shrink-0">
            <a href="https://wa.link/6p3kuz" target="_blank"
              class="inline-flex items-center gap-3 px-10 py-4 rounded-2xl font-semibold text-dark-900 hover:scale-105 transition-all duration-300 shadow-lg"
              style="background: linear-gradient(135deg, #e8c96e, #f59e0b);">
              Mulai Tes Sekarang
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
              </svg>
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const groups = [
  {
    icon: '👨‍👩‍👧',
    title: 'Orang Tua',
    benefits: [
      'Kenali potensi genetik anak sejak dini',
      'Terapkan bahasa cinta yang tepat',
      'Arahkan pendidikan sesuai bakat',
      'Kurangi konflik pola asuh',
    ]
  },
  {
    icon: '🎓',
    title: 'Pelajar & Mahasiswa',
    benefits: [
      'Temukan gaya belajar optimal',
      'Pilih jurusan yang tepat',
      'Kenali kekuatan akademik',
      'Rencanakan karir lebih awal',
    ]
  },
  {
    icon: '💼',
    title: 'Profesional & Dewasa',
    benefits: [
      'Validasi pilihan karir saat ini',
      'Temukan potensi tersembunyi',
      'Kembangkan soft skill',
      'Optimalkan performa kerja',
    ]
  },
  {
    icon: '🏫',
    title: 'Institusi & Sekolah',
    benefits: [
      'Asesmen diagnostik siswa',
      'Pemetaan bakat peserta didik',
      'Komunikasi efektif dengan orang tua',
      'Program pengembangan bakat',
    ]
  }
]
</script>
