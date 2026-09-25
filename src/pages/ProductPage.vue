<script setup>
import ProductCard from '../components/ProductCard.vue';

const daftarProduk = [
  {
  id: 1,
  nama: "sepatu sekolah",
  harga: 150000,
  gambar:"sepatu biru.jpg"
  
  },
  {
    id: 2,
    nama: "tas sekolah",
    harga: 200000,
    gambar:"tas sekolah.jpg"
  },
  {
    id: 3,
    nama: "1 set alat tulis",
    harga: 250000,
    gambar:"1 set alat tulis.jpg"
  },
];  
</script>

<template>
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 p-6">
    <ProductCard
      v-for="produk in daftarProduk"
      :key="produk.id"
      :nama="produk.nama"
      :harga="produk.harga"
      :gambar="produk.gambar"
    />
  </div>
</template>

<style scoped>
.product-page {
  padding: 2rem 0 3rem;
}

.product-page h1 {
  margin-bottom: 1.5rem;
  color:aqua;
}

.grid {
  display:flex;
  flex-wrap: wrap;
  gap: 18px;
}
</style>