<script setup>
import { Icon } from '@iconify/vue';
import { ref } from 'vue';

const why = ref(null)
const scroll = () => {
  why.value?.scrollIntoView()
}
</script>

<template>
  <!-- Main Container dengan padding yang lebih adaptif -->
  <div class="px-6 md:px-16 lg:px-24 bg-slate-50 min-h-screen font-sans">
    
    <!-- Hero Section / Download -->
    <section class="flex flex-col lg:flex-row justify-between min-h-screen items-center gap-12 py-20">
      <div class="flex flex-col gap-8 flex-1 text-center lg:text-left">
        <div class="space-y-2">
          <h1 class="text-blue-950 font-extrabold text-5xl md:text-6xl leading-tight">
            Temukan yang <br>
            <span class="text-yellow-500 italic">Penting.</span> <br>
            <span class="relative inline-block">
              Lebih Cepat.
              <div class="h-2 w-full bg-yellow-200 absolute bottom-2 -z-10"></div>
            </span>
          </h1>
        </div>
        
        <p class="max-w-md mx-auto lg:mx-0 text-blue-900/70 text-lg font-medium leading-relaxed">
          Findit membantu kamu menemukan barang hilang dengan mudah dan cepat. 
          Karena setiap barang berharga, dan setiap penemuan berarti.
        </p>

        <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
          <a href="/Findit.apk" class="bg-blue-950 hover:bg-blue-900 transition-all transform hover:scale-105 px-8 py-4 rounded-xl text-white font-bold shadow-lg shadow-blue-900/20">
            Download Sekarang
          </a>
          <button @click="scroll()" class="border-2 border-blue-950 text-blue-950 px-8 py-4 rounded-xl font-bold hover:bg-blue-50 transition-colors">
            Pelajari Fitur
          </button>
        </div>
      </div>

      <!-- Image Wrapper dengan efek bayangan/floating -->
      <div class="flex-1 w-full max-w-lg relative">
        <div class="absolute -inset-4 bg-yellow-400/20 rounded-full blur-3xl"></div>
        <img 
          class="relative z-10 bg-blue-950 rounded-2xl shadow-2xl w-full object-cover transform -rotate-2 hover:rotate-0 transition-transform duration-500" 
          src="/Putih.png" 
          alt="App Screenshot">
      </div>
    </section>

    <!-- Features Section / Why? -->
    <section ref="why" class="py-24">
      <div class="bg-white border border-blue-100 shadow-xl shadow-blue-900/5 rounded-[2.5rem] p-8 md:p-16">
        <div class="text-center mb-16">
          <h3 class="text-3xl md:text-4xl text-blue-950 font-bold mb-4">Kenapa Pilih Findit?</h3>
          <div class="w-20 h-1.5 bg-yellow-500 mx-auto rounded-full"></div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
          <!-- Feature 1 -->
          <div class="group flex flex-col items-center text-center gap-4 transition-all">
            <div class="bg-sky-100 group-hover:bg-yellow-400 transition-colors duration-300 rounded-2xl w-20 h-20 flex items-center justify-center shadow-sm">
              <Icon icon="material-symbols:search-rounded" class="text-blue-950 text-4xl" />
            </div>
            <h4 class="font-bold text-xl text-blue-950">Mudah & Cepat</h4>
            <p class="text-blue-800/60 text-sm leading-relaxed max-w-[200px]">
              Laporkan kehilangan atau temukan barang dalam hitungan menit tanpa ribet.
            </p>
          </div>

          <!-- Feature 2 -->
          <div class="group flex flex-col items-center text-center gap-4 transition-all">
            <div class="bg-sky-100 group-hover:bg-yellow-400 transition-colors duration-300 rounded-2xl w-20 h-20 flex items-center justify-center shadow-sm">
              <Icon icon="carbon:map" class="text-blue-950 text-4xl" />
            </div>
            <h4 class="font-bold text-xl text-blue-950">Lokasi Akurat</h4>
            <p class="text-blue-800/60 text-sm leading-relaxed max-w-[200px]">
              Lihat lokasi kehilangan atau penemuan di peta secara presisi dan real-time.
            </p>
          </div>

          <!-- Feature 3 -->
          <div class="group flex flex-col items-center text-center gap-4 transition-all">
            <div class="bg-sky-100 group-hover:bg-yellow-400 transition-colors duration-300 rounded-2xl w-20 h-20 flex items-center justify-center shadow-sm">
              <Icon icon="material-symbols:shield-outline" class="text-blue-950 text-4xl" />
            </div>
            <h4 class="font-bold text-xl text-blue-950">Keamanan Terjamin</h4>
            <p class="text-blue-800/60 text-sm leading-relaxed max-w-[200px]">
              Data dan privasi kamu dilindungi dengan sistem enkripsi keamanan terbaik.
            </p>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>