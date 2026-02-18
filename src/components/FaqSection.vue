<template>
  <section id="faq" class="py-32 relative">
    <div class="max-w-4xl mx-auto px-6">
      <div class="text-center mb-20 reveal">
        <span class="font-mono text-xs text-gold tracking-[0.3em] uppercase">FAQ</span>
        <h2 class="mt-4 font-display text-4xl lg:text-6xl font-bold">
          Pertanyaan<br />
          <span class="text-gradient italic">yang Sering Ditanya</span>
        </h2>
      </div>

      <div class="space-y-3">
        <div v-for="(faq, i) in faqs" :key="i" class="reveal glass rounded-2xl overflow-hidden">
          <button @click="toggle(i)"
            class="w-full flex items-center justify-between p-6 text-left hover:bg-white/5 transition-colors">
            <span class="font-medium text-white pr-4">{{ faq.q }}</span>
            <div class="w-7 h-7 rounded-full flex items-center justify-center flex-shrink-0 transition-all duration-300"
              :class="openIndex === i ? 'rotate-45' : ''"
              style="background: rgba(56,189,248,0.1); border: 1px solid rgba(56,189,248,0.2);">
              <svg class="w-3.5 h-3.5 text-brand-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M12 5v14M5 12h14"/>
              </svg>
            </div>
          </button>
          <div v-show="openIndex === i" class="px-6 pb-6">
            <p class="text-slate-400 leading-relaxed">{{ faq.a }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'
const openIndex = ref(0)
const toggle = (i) => { openIndex.value = openIndex.value === i ? null : i }
const faqs = [
  { q: 'Seberapa akurat Tesdia?', a: 'Tesdia telah diikuti ribuan peserta dari anak-anak hingga dewasa. Tingkat kesesuaian hasil berada di atas 85%, berdasarkan feedback dan validasi peserta.' },
  { q: 'Apakah sama dengan Tes IQ?', a: 'Tidak. Tes IQ mengukur kemampuan kognitif saat ini, sedangkan Tesdia mengukur potensi genetik bawaan. Tesdia lebih menyeluruh karena mencakup 8 jenis kecerdasan majemuk, karakter, bahasa cinta, dan gaya belajar.' },
  { q: 'Bagaimana jika rekomendasi profesi tidak sama dengan karir saya?', a: 'Tesdia mengukur "Potensi Genetik", bukan penjara. Dengan mengetahui potensi dan gaya belajar Anda, Anda bisa menjadi apapun — hanya saja dengan cara dan pendekatan yang lebih sesuai dengan diri Anda.' },
  { q: 'Apa beda Tesdia dengan tes sidik jari lain?', a: 'Tesdia menggunakan metode Dermatoglifi yang dipadukan dengan analisis Kecerdasan Majemuk Gardner dan berbasis riset mendalam. Sistem kami terus diperbarui dan dilengkapi konsultasi personal oleh konsultan tersertifikasi.' },
  { q: 'Bagaimana jika sidik jari saya tidak terdeteksi?', a: 'Sidik jari yang rusak (bekas luka, kecelakaan, atau kelainan genetik) mungkin tidak terbaca sempurna. Jika satu atau lebih sidik jari tidak terbaca, hal ini akan mengurangi akurasi hasil. Tim kami siap membantu mencari solusi terbaik.' },
  { q: 'Apakah perlu tes ulang di kemudian hari?', a: 'Tidak perlu. Sidik jari bersifat permanen dan tidak berubah sejak bayi lahir. Cukup satu kali tes DIA seumur hidup untuk mendapatkan peta potensi genetik Anda yang akurat.' },
]
</script>
