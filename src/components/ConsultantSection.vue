<template>
  <section id="konsultan" class="py-32 relative">
    <div class="max-w-7xl mx-auto px-6">
      <div class="text-center mb-20 reveal">
        <span class="font-mono text-xs text-brand-400 tracking-[0.3em] uppercase">Tim Konsultan</span>
        <h2 class="mt-4 font-display text-4xl lg:text-6xl font-bold">
          Konsultan<br />
          <span class="text-gradient italic">Bersertifikasi Kami</span>
        </h2>
        <p class="mt-6 text-slate-400 max-w-xl mx-auto">Tersebar di berbagai kota di Sumatera Utara dan terus berkembang. Hubungi konsultan terdekat Anda.</p>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-5">
        <div v-for="(c, i) in consultants" :key="i"
          class="reveal glass rounded-3xl p-7 hover:border-white/15 transition-all duration-500 group"
          :style="{ transitionDelay: i * 80 + 'ms' }">
          <div class="flex items-start gap-4">
            <div class="w-12 h-12 rounded-2xl flex items-center justify-center text-xl font-display font-bold flex-shrink-0"
              :style="{ background: 'linear-gradient(135deg, ' + c.color + '30, ' + c.color + '10)', border: '1px solid ' + c.color + '30', color: c.color }">
              {{ c.name.charAt(0) }}
            </div>
            <div class="min-w-0">
              <span class="text-xs font-mono text-slate-600">{{ c.region }}</span>
              <h3 class="text-white font-semibold mt-0.5 text-sm leading-tight">{{ c.name }}</h3>
              <p class="text-slate-500 text-xs mt-0.5">{{ c.title }}</p>
            </div>
          </div>
          <div class="mt-5 pt-5 border-t border-white/5 space-y-2">
            <p class="text-slate-500 text-xs flex items-start gap-2">
              <svg class="w-3.5 h-3.5 mt-0.5 text-slate-600 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
              </svg>
              {{ c.address }}
            </p>
            <a :href="'https://wa.me/' + c.phone.replace(/\D/g, '')" target="_blank"
              class="flex items-center gap-2 text-xs text-brand-400 hover:text-brand-300 transition-colors">
              <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 24 24">
                <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/>
              </svg>
              {{ c.phone }}
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const consultants = [
  { name: 'Rahmat Mulyanoor, S.E., MHA', title: 'Office Center / Pusat', region: 'Pusat', address: 'Deli Serdang, Sumatera Utara', phone: '0896-8145-9473', color: '#38bdf8' },
  { name: 'Ns Martoni Calvein', title: 'Konsultan Medan', region: 'Kota Medan', address: 'Jln Cardiac Center, depan paviliun RSUP H Adam Malik', phone: '081269151387', color: '#e8c96e' },
  { name: 'Seftiana Sari, S.Ked, M.Psi', title: 'Smart Aurica School', region: 'Kota Medan', address: 'Jl. Sei Batang Hari No.114, Babura Sunggal, Medan', phone: '081264644985', color: '#818cf8' },
  { name: 'H. Syamsul Bahri, M.Pd', title: 'Showroom Mobilku', region: 'Kota Medan', address: 'Jl Nibung Raya No.183, Medan Petisah', phone: '085262904209', color: '#34d399' },
  { name: 'Anugrah Halilk, S.Pd', title: 'Konsultan Deli Serdang', region: 'Deli Serdang', address: 'Jl. Sidomulyo Gg. Merpati, Kec. Percut Sei Tuan', phone: '085359815074', color: '#f472b6' },
  { name: 'Dr. Muhammad Saleh, MA, CPM', title: 'Bimbel Insan Cendekia', region: 'Langkat', address: 'Jln Tawang Mangu Ling.1 Kel. Kwala Bingai, Stabat', phone: '081361362126', color: '#fb923c' },
]
</script>
