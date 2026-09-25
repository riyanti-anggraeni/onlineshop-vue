<script setup>
import ProductCard from '../components/ProductCard.vue'

const daftarProduk = [
  {
    id: 1,
    nama: 'Sepatu Sekolah',
    harga: 150000,
    gambar: 'https://i.pinimg.com/736x/1a/77/5a/1a775a9f96d076f29aecaff677dadfb9.jpg'
  },
  {
    id: 2,
    nama: 'Tas Sekolah',
    harga: 200000,
    gambar: 'https://i.pinimg.com/736x/e4/bb/8f/e4bb8fa554b975c2ff93582f4c0ed2e2.jpg'
  },
  {
    id: 3,
    nama: '1 Set Alat Tulis',
    harga: 250000,
    gambar: 'https://i.pinimg.com/736x/e1/6a/8a/e16a8a2db6af6628aa34372b9ebc9b0e.jpg'
  }
]
</script>

<template>
  <div class="product-page">

    <!-- HEADER -->
    <section class="product-header">

      <div class="badge">
        🎒 OUR PRODUCTS
      </div>

      <h1>
        Perlengkapan <span>Sekolah</span>
      </h1>

      <p>
        Temukan berbagai kebutuhan sekolah
        dengan harga yang bersahabat.
      </p>

    </section>


    <!-- DAFTAR PRODUK -->
    <section class="product-list">

      <ProductCard
        v-for="produk in daftarProduk"
        :key="produk.id"
        :nama="produk.nama"
        :harga="produk.harga"
        :gambar="produk.gambar"
      />

    </section>

  </div>
</template>


<style scoped>

* {
  box-sizing: border-box;
  font-family: 'Segoe UI', Arial, sans-serif;
}


/* ================================
   PRODUCT PAGE
================================ */

.product-page {
  min-height: 100vh;

  padding: 60px 60px 100px;

  background: linear-gradient(
    180deg,
    #bfdbfe 0%,
    #dbeafe 45%,
    #eff6ff 100%
  );

  color: #172554;
}


/* ================================
   HEADER
================================ */

.product-header {
  text-align: center;

  margin-bottom: 50px;
}

.badge {
  display: inline-block;

  padding: 9px 18px;

  margin-bottom: 15px;

  border-radius: 30px;

  background: #2563eb;

  color: white;

  font-size: 11px;

  font-weight: 800;

  letter-spacing: 2px;

  box-shadow:
    0 8px 20px rgba(37, 99, 235, 0.25);
}

.product-header h1 {
  margin: 10px 0;

  font-size: 42px;

  font-weight: 800;

  color: #172554;
}

.product-header h1 span {
  color: #2563eb;
}

.product-header p {
  max-width: 500px;

  margin: 0 auto;

  color: #475569;

  font-size: 15px;

  line-height: 1.7;
}


/* ================================
   PRODUCT GRID
================================ */

.product-list {
  max-width: 1100px;

  margin: auto;

  display: grid;

  grid-template-columns: repeat(3, 1fr);

  gap: 25px;
}


/* ================================
   RESPONSIVE
================================ */

@media (max-width: 900px) {

  .product-page {
    padding: 50px 25px 80px;
  }

  .product-list {
    grid-template-columns: repeat(2, 1fr);
  }

}


@media (max-width: 600px) {

  .product-page {
    padding: 40px 20px 60px;
  }

  .product-list {
    grid-template-columns: 1fr;
  }

  .product-header h1 {
    font-size: 30px;
  }

}

</style>