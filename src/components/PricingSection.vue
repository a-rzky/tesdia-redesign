<template>
  <section id="harga" class="py-32 relative">
    <div class="absolute inset-0" style="background: radial-gradient(ellipse at 30% 50%, rgba(3, 105, 161, 0.08) 0%, transparent 60%);"></div>
    
    <div class="max-w-7xl mx-auto px-6">
      <div class="text-center mb-20 reveal">
        <span class="font-mono text-xs text-brand-400 tracking-[0.3em] uppercase">Harga Paket</span>
        <h2 class="mt-4 font-display text-4xl lg:text-6xl font-bold">
          Investasi Sekali,<br />
          <span class="text-gradient italic">Manfaat Seumur Hidup</span>
        </h2>
        <p class="mt-6 text-slate-400 max-w-xl mx-auto">Pilih paket yang sesuai. Semua paket sudah termasuk e-sertifikat dan penjelasan dari konsultan tersertifikasi.</p>
      </div>

      <div class="grid md:grid-cols-3 gap-6 max-w-5xl mx-auto">
        <div v-for="(plan, i) in plans" :key="i"
          class="reveal rounded-3xl p-8 relative overflow-hidden transition-all duration-500 hover:-translate-y-2"
          :class="plan.popular ? 'border border-gold/40' : 'glass'"
          :style="plan.popular ? 'background: linear-gradient(160deg, rgba(232,201,110,0.12), rgba(14,165,233,0.06))' : ''">
          
          <!-- Popular badge -->
          <div v-if="plan.popular" class="absolute top-6 right-6">
            <span class="px-3 py-1 rounded-full text-xs font-mono font-bold text-dark-900" style="background: linear-gradient(135deg, #e8c96e, #f59e0b);">
              TERLARIS
            </span>
          </div>

          <div class="space-y-6">
            <div>
              <h3 class="font-display text-2xl font-bold" :class="plan.popular ? 'text-gold' : 'text-white'">{{ plan.name }}</h3>
              <p class="text-slate-500 text-sm mt-1">{{ plan.subtitle }}</p>
            </div>

            <div>
              <div class="text-slate-600 line-through text-sm">{{ plan.originalPrice }}</div>
              <div class="flex items-end gap-2 mt-1">
                <span class="font-display text-4xl font-bold text-white">{{ plan.price }}</span>
              </div>
              <div class="text-slate-500 text-xs mt-1">{{ plan.for }}</div>
            </div>

            <ul class="space-y-3">
              <li v-for="feature in plan.features" :key="feature" class="flex items-center gap-3 text-sm text-slate-300">
                <div class="w-5 h-5 rounded-full flex items-center justify-center flex-shrink-0"
                  :style="{ background: plan.popular ? 'rgba(232,201,110,0.2)' : 'rgba(56,189,248,0.15)', border: plan.popular ? '1px solid rgba(232,201,110,0.4)' : '1px solid rgba(56,189,248,0.3)' }">
                  <svg class="w-3 h-3" :class="plan.popular ? 'text-gold' : 'text-brand-400'" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                  </svg>
                </div>
                {{ feature }}
              </li>
            </ul>

            <a :href="plan.link" target="_blank"
              class="block w-full text-center py-4 rounded-2xl font-semibold transition-all duration-300 hover:scale-105"
              :class="plan.popular
                ? 'text-dark-900 hover:shadow-xl'
                : 'glass text-white hover:bg-white/10'"
              :style="plan.popular ? 'background: linear-gradient(135deg, #e8c96e, #f59e0b)' : ''">
              Konsultasi Sekarang
            </a>
          </div>
        </div>
      </div>

      <!-- Partnership note -->
      <div class="text-center mt-12 reveal">
        <p class="text-slate-500 text-sm">Butuh paket untuk institusi atau sekolah?</p>
        <a href="https://tesdia.id/kemitraan/" target="_blank" class="text-brand-400 hover:text-brand-300 text-sm font-medium mt-1 inline-block transition-colors">
          Lihat Program Kemitraan →
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
const plans = [
  {
    name: 'Reguler',
    subtitle: 'Untuk individu',
    originalPrice: 'Rp 650.000',
    price: 'Rp 450.000',
    for: 'per orang',
    popular: false,
    link: 'https://wa.link/iqmpch',
    features: [
      'Tes untuk 1 orang',
      'E-Sertifikat hasil tes',
      'Report analisis lengkap',
      'Penjelasan oleh konsultan',
    ]
  },
  {
    name: 'Friendly',
    subtitle: 'Paket berdua',
    originalPrice: 'Rp 1.300.000',
    price: 'Rp 750.000',
    for: 'paket 2 orang',
    popular: true,
    link: 'https://wa.link/hsmejb',
    features: [
      'Tes untuk 2 orang',
      'E-Sertifikat tiap peserta',
      'Report analisis lengkap',
      'Penjelasan oleh konsultan',
      'Konsultasi online*',
    ]
  },
  {
    name: 'Family',
    subtitle: 'Paket keluarga',
    originalPrice: 'Rp 1.550.000',
    price: 'Rp 950.000',
    for: 'paket 3 orang',
    popular: false,
    link: 'https://wa.link/a42n4y',
    features: [
      'Tes untuk 3 orang',
      'E-Sertifikat tiap peserta',
      'Report analisis lengkap',
      'Penjelasan oleh konsultan',
      'Konsultasi online*',
    ]
  }
]
</script>
