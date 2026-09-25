<script setup>
const scrollToProduct = () => {
  alert('Nanti arahkan ke halaman Product ya!');
}
</script>

<template>
 

    <section class="hero">
      <h1>Belanja Perlengkapan Sekolah, Gampang &<br>Terpercaya</h1>
      <p>Dari kaos, topi, sampai tas sekolah — semua ada di satu tempat.</p>
      <button class="btn" @click="scrollToProduct">Lihat Produk</button>
    </section>

    <section class="features">
      <div class="feature">
        <div class="icon"></div>
        <h3>Kualitas Terjamin</h3>
        <p>Bahan dipilih langsung oleh tim sekolah</p>
      </div>
      <div class="feature">
        <div class="icon"></div>
        <h3>Harga Bersahabat</h3>
        <p>Harga ramah di kantong siswa</p>
      </div>
      <div class="feature">
        <div class="icon"></div>
        <h3>Ambil di Sekolah</h3>
        <p>Tidak perlu ongkir, ambil di koperasi</p>
      </div>
    </section>
  <!-- VIDEO PROMOSI -->
<section class="video-section">
  
  <video controls width="100%" style="max-width:700px; border-radius:12px;">
    <source src="./assets/mov_bbb.mp4" type="video/mp4" />
    Browser lu gak support video.
  </video>
</section>
</template>

<style scoped>
* { font-family: 'Segoe UI', Arial, sans-serif; }
.page { background: #f8fafc; min-height: 100vh; }
.navbar {
  display: flex; justify-content: space-between;
  padding: 15px 80px; background: white;
  font-size: 14px; font-weight: 600;
}
.navbar a { text-decoration: none; color: #333; margin-left: 15px; }
.navbar a:hover { color: #1e88e5; }

.hero {
  background: linear-gradient(135deg, #42a5f5, #1565c0);
  color: white; text-align: center;
  padding: 70px 20px; margin: 0 80px;
}
.hero h1 { font-size: 32px; font-weight: 800; margin-bottom: 15px; }
.hero p { font-size: 14px; opacity: 0.9; margin-bottom: 25px; }
.btn {
  background: white; color: #1565c0; border: none;
  padding: 12px 28px; border-radius: 25px;
  font-weight: 700; cursor: pointer;
}
.btn:hover { transform: scale(1.05); }

.features {
  display: flex; justify-content: center; gap: 80px;
  padding: 60px 80px; text-align: center;
  background: white; margin: 0 80px;
}
.feature { max-width: 220px; }
.icon { font-size: 28px; margin-bottom: 10px; }
.feature h3 { font-size: 14px; margin-bottom: 6px; }
.feature p { font-size: 11px; color: #777; }
</style>