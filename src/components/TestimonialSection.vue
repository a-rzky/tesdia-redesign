<template>
  <section id="testimoni" class="py-32 relative overflow-hidden">
    <div class="absolute inset-0" style="background: radial-gradient(ellipse at 60% 40%, rgba(129,140,248,0.05) 0%, transparent 60%);"></div>

    <div class="max-w-7xl mx-auto px-6">
      <div class="text-center mb-20 reveal">
        <span class="font-mono text-xs text-brand-400 tracking-[0.3em] uppercase">Testimoni</span>
        <h2 class="mt-4 font-display text-4xl lg:text-6xl font-bold">
          Apa Kata<br />
          <span class="text-gradient-blue italic">Mereka?</span>
        </h2>
      </div>

      <!-- Masonry-style grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-5">
        <div v-for="(t, i) in testimonials" :key="i"
          class="reveal glass rounded-3xl p-7 hover:border-white/15 transition-all duration-500"
          :class="t.featured ? 'md:col-span-2 lg:col-span-1' : ''"
          :style="{ transitionDelay: i * 80 + 'ms' }">
          <!-- Stars -->
          <div class="flex gap-1 mb-5">
            <svg v-for="s in 5" :key="s" class="w-4 h-4" :class="s <= t.rating ? 'text-gold' : 'text-slate-700'" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
            </svg>
          </div>
          
          <p class="text-slate-300 leading-relaxed mb-6 italic">"{{ t.text }}"</p>
          
          <div class="flex items-center gap-3">
            <div class="w-10 h-10 rounded-full flex items-center justify-center text-lg font-display font-bold"
              :style="{ background: 'linear-gradient(135deg, ' + t.color + '40, ' + t.color + '10)', border: '1px solid ' + t.color + '30', color: t.color }">
              {{ t.name.charAt(0) }}
            </div>
            <div>
              <div class="text-white font-medium text-sm">{{ t.name }}</div>
              <div class="text-slate-600 text-xs">{{ t.role }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    name: 'Wiwik',
    role: 'Kepala Sekolah TK',
    rating: 4,
    text: 'Kami sudah menggunakan Tesdia ini di 4 kali penerimaan siswa baru! Ini memudahkan kami berkomunikasi dengan orang tua terkait anak didik. Guru terdidik, orang tua terdidik, anak bahagia.',
    color: '#38bdf8',
    featured: true,
  },
  {
    name: 'Marwoto',
    role: 'Penilik PAUD',
    rating: 5,
    text: 'Tes ini membantu saya menjalani profesi sebagai kepala sekolah yang dicintai. Dengan tes ini saya mampu menerapkan bahasa cinta ke masing-masing anak, karena saya mengetahuinya.',
    color: '#e8c96e',
    featured: false,
  },
  {
    name: 'Mujiono',
    role: 'Ka. Seksi Pendidikan',
    rating: 5,
    text: 'Asesmen diagnostik tidak perlu repot-repot dengan waktu lama dan dokumen bertumpuk. Hari ini kita dimudahkan dengan teknologi yang mudah, murah, dan akurat.',
    color: '#818cf8',
    featured: false,
  },
  {
    name: 'Rina S.',
    role: 'Ibu Rumah Tangga, Medan',
    rating: 5,
    text: 'Saya akhirnya mengerti kenapa anak saya lebih suka belajar sambil bergerak. Setelah tes DIA, saya tahu cara yang tepat mendukungnya. Nilai rapor langsung naik!',
    color: '#34d399',
    featured: false,
  },
  {
    name: 'Budi H.',
    role: 'Mahasiswa Semester 3',
    rating: 4,
    text: 'Tadinya bingung mau ambil jurusan apa. Setelah tes DIA, saya lebih yakin dengan pilihan saya. Ternyata passion saya memang di bidang yang sudah saya pilih.',
    color: '#f472b6',
    featured: false,
  },
  {
    name: 'Sari W.',
    role: 'HRD Manager',
    rating: 5,
    text: 'Kami pakai Tesdia untuk asesmen karyawan baru. Hasilnya sangat membantu dalam penempatan posisi yang sesuai karakter dan potensi mereka.',
    color: '#fb923c',
    featured: false,
  },
]
</script>
