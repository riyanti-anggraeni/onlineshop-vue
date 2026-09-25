<script setup>
import { ref } from 'vue';
defineProps(["nama", "harga", "gambar"]);
const gambarDipilih = ref(null);
function bukaPreview(src) {
  gambarDipilih.value = src;
}
 
function tutupPreview() {
  gambarDipilih.value = null
}
function tambahKeranjang(nama){
    const suara = new audio("")
    suara.play();
    alert(`${nama} di tambahkan ke keranjang`);
}
</script>
<template>
  <div class="bg-white rounded-x1 shadow-md p-4 hover:shadpw-lg transition">
    <img :src="gambar"
     :alt="nama" 
     @click="bukaPreview(gambar)"
     class="w-full h-40 object-cover rounded-lg cursor-pointer"
     />
    <h3 class=text-lg font-semibold m-2>{{ nama }}</h3>
    <p class="text-gray-600">Rp {{ harga.toLocaleString('id-ID') }}</p>
    <button
    @click="tambahKeranjang(nama)"
    class="bg-pink-200 text-white px-4 py2 rounded-lg mt-2 w-full hover:bgpink-600">
  </button>
  </div>
 <!-- AUDIO -->
<section class="audio-section">
  
  <audio controls style="margin-top:15px; width: 300px;">
    <source src="./assets/nikin-pop-up-something-160353.mp3" type="audio/mpeg" />
  </audio>
</section>
  <div
   v-if="gambarDipilih"
    class="fixed inset-0 bg-black/70 flex items-center justifycenter cursor-zoom-out">
     @click="tutupPreview">
    <img :src="gambarDipilih" class="max-w-[80%] max-h-[80%] rounded-lg" />
  </div>
</template>
 
<style scoped>
.preview-overlay {
  position: fixed;
   top: 0; left: 0;
    width: 100%;
     height: 100%;
  background: rgba(0,0,0,0.7);
  display: flex; align-items: center; justify-content: center;
}
.preview-besar { max-width: 80%; max-height: 80%; border-radius: 8px; }
</style>
 
