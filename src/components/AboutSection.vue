<template>
  <section id="tentang" class="py-32 relative">
    <div class="max-w-7xl mx-auto px-6">
      <!-- Section Header -->
      <div class="text-center mb-20 reveal">
        <span class="font-mono text-xs text-brand-400 tracking-[0.3em] uppercase">Mengapa Tes DIA?</span>
        <h2 class="mt-4 font-display text-4xl lg:text-6xl font-bold">
          Kenali Diri Lebih<br />
          <span class="text-gradient italic">Dalam & Akurat</span>
        </h2>
        <p class="mt-6 text-slate-400 max-w-2xl mx-auto text-lg">
          DIA (Dermatoglyphics Intelligence Analysis) adalah ilmu yang menganalisis pola unik sidik jari Anda untuk mengungkap kekuatan genetik yang tersembunyi.
        </p>
      </div>

      <!-- How It Works -->
      <div class="grid md:grid-cols-3 gap-6 mb-20">
        <div v-for="(step, i) in steps" :key="i" class="reveal glass rounded-3xl p-8 relative overflow-hidden group hover:border-brand-500/30 transition-all duration-500">
          <div class="absolute top-0 right-0 w-32 h-32 rounded-full opacity-5 group-hover:opacity-10 transition-opacity"
            :style="{ background: step.color, transform: 'translate(30%, -30%)' }"></div>
          <div class="w-12 h-12 rounded-2xl flex items-center justify-center mb-6 text-xl" :style="{ background: step.color + '20', border: '1px solid ' + step.color + '40' }">
            {{ step.icon }}
          </div>
          <div class="font-mono text-xs text-slate-600 mb-2">LANGKAH 0{{ i + 1 }}</div>
          <h3 class="font-display text-xl font-semibold text-white mb-3">{{ step.title }}</h3>
          <p class="text-slate-400 text-sm leading-relaxed">{{ step.desc }}</p>
        </div>
      </div>

      <!-- Feature Grid -->
      <div class="grid lg:grid-cols-2 gap-6">
        <div class="glass rounded-3xl p-10 reveal space-y-6">
          <h3 class="font-display text-3xl font-bold">Apa Yang Akan Anda Ketahui?</h3>
          <div class="space-y-4">
            <div v-for="item in insights" :key="item.title" class="flex items-start gap-4 group">
              <div class="w-10 h-10 rounded-xl flex items-center justify-center flex-shrink-0 transition-all group-hover:scale-110"
                style="background: rgba(56, 189, 248, 0.1); border: 1px solid rgba(56, 189, 248, 0.2);">
                <span class="text-lg">{{ item.icon }}</span>
              </div>
              <div>
                <div class="text-white font-medium">{{ item.title }}</div>
                <div class="text-slate-500 text-sm mt-0.5">{{ item.desc }}</div>
              </div>
            </div>
          </div>
        </div>

        <div class="glass rounded-3xl p-10 reveal flex flex-col justify-between"
          style="background: linear-gradient(135deg, rgba(14, 165, 233, 0.1), rgba(129, 140, 248, 0.05));">
          <div>
            <span class="font-mono text-xs text-gold tracking-widest">TEKNOLOGI</span>
            <h3 class="font-display text-3xl font-bold mt-3">Akurat & Terpercaya</h3>
            <p class="text-slate-400 mt-4 leading-relaxed">
              Berbasis penelitian dermatoglifi yang telah berlangsung selama lebih dari 200 tahun. Sidik jari terbentuk sejak janin berusia 13 minggu dan tidak berubah seumur hidup — menjadikannya peta genetik paling autentik.
            </p>
          </div>
          <div class="grid grid-cols-2 gap-4 mt-8">
            <div v-for="fact in facts" :key="fact.value" class="glass-gold rounded-2xl p-4 text-center">
              <div class="font-display text-2xl font-bold text-gold">{{ fact.value }}</div>
              <div class="text-xs text-slate-500 mt-1">{{ fact.label }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  { icon: '🖐️', title: 'Scan 10 Sidik Jari', desc: 'Proses pemindaian mudah dan cepat melalui aplikasi atau perangkat khusus kami. Hanya butuh beberapa menit.', color: '#0ea5e9' },
  { icon: '⚡', title: 'Analisis AI + Dermatoglifi', desc: 'Sistem kami menganalisis pola, ridge, dan komposisi sidik jari dengan algoritma yang sudah teruji.', color: '#e8c96e' },
  { icon: '📋', title: 'Report & Konsultasi', desc: 'Dapatkan laporan lengkap dan sertifikat digital, plus sesi konsultasi bersama konsultan tersertifikasi.', color: '#818cf8' },
]
const insights = [
  { icon: '🧠', title: 'Kecerdasan Majemuk (Multiple Intelligence)', desc: 'Linguistik, logika, musikal, spasial, kinestetik, naturalis, interpersonal, intrapersonal' },
  { icon: '❤️', title: 'Bahasa Cinta & Gaya Komunikasi', desc: 'Memahami cara Anda memberi dan menerima kasih sayang' },
  { icon: '📖', title: 'Gaya Belajar & Dominasi Otak', desc: 'Visual, auditori, atau kinestetik — temukan cara belajar paling efektif' },
  { icon: '💼', title: 'Rekomendasi Profesi & Karir', desc: 'Bidang pekerjaan yang paling sesuai dengan potensi genetik Anda' },
  { icon: '🌟', title: 'Karakter & Kepribadian', desc: 'Kekuatan intrinsik yang menjadi fondasi kesuksesan Anda' },
]
const facts = [
  { value: '85%+', label: 'Tingkat Akurasi' },
  { value: '200+', label: 'Tahun Riset' },
  { value: '1×', label: 'Tes Seumur Hidup' },
  { value: '5000+', label: 'Peserta Indonesia' },
]
</script>
