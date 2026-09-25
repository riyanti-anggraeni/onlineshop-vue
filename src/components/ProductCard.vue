<script setup>
import { ref } from 'vue'

defineProps(['nama', 'harga', 'gambar'])

const gambarDipilih = ref(null)

function bukaPreview(src) {
  gambarDipilih.value = src
}

function tutupPreview() {
  gambarDipilih.value = null
}
</script>

<template>

  <!-- PRODUCT CARD -->
  <div class="card">

    <!-- GAMBAR PRODUK -->
    <div class="gambar-container">
      <img
        :src="gambar"
        :alt="nama"
        @click="bukaPreview(gambar)"
      />
    </div>

    <!-- INFORMASI PRODUK -->
    <div class="product-info">

      <h3>
        {{ nama }}
      </h3>

      <p class="harga">
        Rp {{ harga.toLocaleString('id-ID') }}
      </p>

      <!-- BUTTON BELI -->
      <button class="button-beli">
        Beli
      </button>

    </div>

  </div>


  <!-- PREVIEW GAMBAR -->
  <div
    v-if="gambarDipilih"
    class="preview-overlay"
    @click="tutupPreview"
  >

    <img
      :src="gambarDipilih"
      class="preview-besar"
    />

  </div>

</template>


<style scoped>

/* ================================
   CARD
================================ */

.card {
  width: 100%;

  background: white;

  border: 1px solid #bfdbfe;

  border-radius: 22px;

  overflow: hidden;

  box-shadow:
    0 10px 25px rgba(37, 99, 235, 0.12);

  transition: 0.3s ease;
}


/* CARD HOVER */

.card:hover {
  transform: translateY(-7px);

  box-shadow:
    0 18px 35px rgba(37, 99, 235, 0.22);
}


/* ================================
   GAMBAR
================================ */

.gambar-container {
  width: 100%;

  height: 230px;

  overflow: hidden;

  background: #eff6ff;
}

.gambar-container img {
  width: 100%;

  height: 100%;

  display: block;

  object-fit: cover;

  cursor: zoom-in;

  transition: transform 0.3s ease;
}


/* EFEK GAMBAR */

.card:hover .gambar-container img {
  transform: scale(1.05);
}


/* ================================
   PRODUCT INFO
================================ */

.product-info {
  padding: 20px;
}

.product-info h3 {
  margin: 0 0 10px;

  color: #172554;

  font-size: 18px;

  font-weight: 700;
}


/* ================================
   HARGA
================================ */

.harga {
  margin: 0 0 16px;

  color: #2563eb;

  font-size: 18px;

  font-weight: 800;
}


/* ================================
   BUTTON BELI
================================ */

.button-beli {
  width: 100%;

  padding: 12px 20px;

  border: none;

  border-radius: 12px;

  background: #2563eb;

  color: white;

  font-size: 14px;

  font-weight: 700;

  cursor: pointer;

  transition: 0.25s ease;
}


/* BUTTON HOVER */

.button-beli:hover {
  background: #1d4ed8;

  transform: translateY(-2px);

  box-shadow:
    0 8px 18px rgba(37, 99, 235, 0.3);
}


/* BUTTON ACTIVE */

.button-beli:active {
  transform: scale(0.98);
}


/* ================================
   PREVIEW OVERLAY
================================ */

.preview-overlay {
  position: fixed;

  top: 0;
  left: 0;

  width: 100%;
  height: 100%;

  background: rgba(15, 23, 42, 0.75);

  display: flex;

  align-items: center;
  justify-content: center;

  cursor: zoom-out;

  z-index: 9999;

  padding: 30px;
}


/* GAMBAR BESAR */

.preview-besar {
  max-width: 80%;

  max-height: 80%;

  border-radius: 15px;

  box-shadow:
    0 20px 50px rgba(0, 0, 0, 0.35);

  object-fit: contain;
}


/* ================================
   RESPONSIVE
================================ */

@media (max-width: 600px) {

  .gambar-container {
    height: 210px;
  }

  .product-info {
    padding: 18px;
  }

  .preview-besar {
    max-width: 90%;
    max-height: 80%;
  }

}

</style>