<template>
  <footer class="relative border-t border-white/5 py-20">
    <div class="max-w-7xl mx-auto px-6">
      <!-- Top CTA -->
      <div class="text-center mb-20">
        <h2 class="font-display text-4xl lg:text-5xl font-bold mb-6">
          Siap Kenali<br />
          <span class="text-gradient italic">Potensi Terbaik Anda?</span>
        </h2>
        <a href="https://wa.link/6p3kuz" target="_blank"
          class="inline-flex items-center gap-3 px-10 py-4 rounded-2xl font-semibold text-dark-900 hover:scale-105 transition-all duration-300 shadow-xl"
          style="background: linear-gradient(135deg, #e8c96e, #f59e0b);">
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
            <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
          </svg>
          Mulai Konsultasi via WhatsApp
        </a>
      </div>

      <!-- Footer Links -->
      <div class="grid md:grid-cols-4 gap-10 border-t border-white/5 pt-12">
        <div class="md:col-span-2">
          <div class="flex items-center gap-3 mb-4">
            <div class="w-9 h-9 rounded-xl flex items-center justify-center" style="background: linear-gradient(135deg, #e8c96e, #0ea5e9);">
              <span class="text-dark-900 font-mono font-bold text-sm">DIA</span>
            </div>
            <span class="font-display text-xl text-white font-semibold">Tes<span class="text-gradient">DIA</span></span>
          </div>
          <p class="text-slate-500 text-sm leading-relaxed max-w-sm">
            Dermatoglyphics Intelligence Analysis — teknologi analisis sidik jari untuk mengungkap potensi genetik terbaik Anda.
          </p>
          <p class="text-slate-600 text-xs mt-4">by PT. RIM Edukasi Indonesia</p>
        </div>

        <div>
          <h4 class="text-white font-semibold text-sm mb-4">Navigasi</h4>
          <ul class="space-y-2.5">
            <li v-for="link in navLinks" :key="link.label">
              <a :href="link.href" class="text-slate-500 text-sm hover:text-white transition-colors">{{ link.label }}</a>
            </li>
          </ul>
        </div>

        <div>
          <h4 class="text-white font-semibold text-sm mb-4">Kontak</h4>
          <ul class="space-y-2.5">
            <li><a href="https://wa.link/6p3kuz" target="_blank" class="text-slate-500 text-sm hover:text-white transition-colors flex items-center gap-2">
              <span>💬</span> WhatsApp
            </a></li>
            <li><a href="https://apps2.tesdia.id/" target="_blank" class="text-slate-500 text-sm hover:text-white transition-colors flex items-center gap-2">
              <span>🔗</span> Portal Peserta
            </a></li>
            <li><a href="https://tesdia.id/kemitraan/" target="_blank" class="text-slate-500 text-sm hover:text-white transition-colors flex items-center gap-2">
              <span>🤝</span> Kemitraan
            </a></li>
            <li><a href="http://tesdia.id/article-list/" target="_blank" class="text-slate-500 text-sm hover:text-white transition-colors flex items-center gap-2">
              <span>📝</span> Blog
            </a></li>
          </ul>
        </div>
      </div>

      <div class="border-t border-white/5 mt-10 pt-8 flex flex-col md:flex-row justify-between items-center gap-4">
        <p class="text-slate-700 text-xs">© 2024 TES DIA — PT. RIM Edukasi Indonesia. All rights reserved.</p>
        <p class="text-slate-700 text-xs">Redesigned with ❤️ for better experience</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
const navLinks = [
  { label: 'Tentang DIA', href: '#tentang' },
  { label: 'Manfaat', href: '#manfaat' },
  { label: 'Harga', href: '#harga' },
  { label: 'Testimoni', href: '#testimoni' },
  { label: 'FAQ', href: '#faq' },
  { label: 'Konsultan', href: '#konsultan' },
]
</script>
