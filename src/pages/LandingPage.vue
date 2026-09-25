<script setup>
const scrollToProduct = () => {
  alert('Nanti arahkan ke halaman Product ya!')
}
</script>

<template>
  <div class="page">

    <section class="hero">
      <div class="hero-content">

        <span class="badge">
          🎒 SCHOOL STORE
        </span>

        <h1>
          Semua Kebutuhan Sekolah,
          <span>Dalam Satu Tempat.</span>
        </h1>

        <p class="hero-description">
          Cari perlengkapan sekolah dengan mudah,
          harga bersahabat, dan bisa diambil langsung di sekolah.
        </p>

        <button class="btn" @click="scrollToProduct">
          Lihat Produk
          <span>→</span>
        </button>

      </div>

      <div class="hero-decoration">
        🎒
      </div>
    </section>

    <section class="features">

      <div class="section-title">
        <span>WHY US?</span>
        <h2>Kenapa Belanja di Sini?</h2>
      </div>

      <div class="feature-container">

        <div class="feature">
          <div class="icon blue">✓</div>

          <div>
            <h3>Kualitas Terjamin</h3>
            <p>
              Produk dipilih dengan kualitas terbaik
              untuk kebutuhan sekolah.
            </p>
          </div>
        </div>

        <div class="feature">
          <div class="icon blue">♡</div>

          <div>
            <h3>Harga Bersahabat</h3>
            <p>
              Harga dibuat ramah di kantong
              siswa dan pelajar.
            </p>
          </div>
        </div>

        <div class="feature">
          <div class="icon blue">⌂</div>

          <div>
            <h3>Ambil di Sekolah</h3>
            <p>
              Nggak perlu repot bayar ongkir,
              tinggal ambil di koperasi.
            </p>
          </div>
        </div>

      </div>
    </section>

    <section class="video-section">

      <div class="video-text">
        <span>OUR STORE</span>

        <h2>
          Lihat Keseruannya
          <br />
          <strong>di Sekolah!</strong>
        </h2>

        <p>
          Kenalan lebih dekat dengan layanan
          dan produk yang tersedia di school store kami.
        </p>
      </div>

      <div class="video-box">
        <video controls>
          <source
            src="/video/mov_bbb.mp4"
            type="video/mp4"
          />
          Browser kamu tidak mendukung video.
        </video>
      </div>

    </section>

    <section class="cta">

      <div>
        <span>READY TO SHOP?</span>

        <h2>
          Yuk, cari kebutuhan
          sekolahmu! 🎒
        </h2>
      </div>

      <button @click="scrollToProduct">
        Mulai Belanja →
      </button>

    </section>

    <footer>
      <p>
        © 2026 School Store.
        Made for students.
      </p>
    </footer>

  </div>
</template>

<style scoped>

/* ================================
   GLOBAL
================================ */

* {
  font-family: 'Segoe UI', Arial, sans-serif;
  box-sizing: border-box;
}

.page {
  min-height: 100vh;
  background: linear-gradient(
    180deg,
    #dbeafe 0%,
    #eff6ff 50%,
    #bfdbfe 100%
  );

  color: #172554;
}

/* ================================
   HERO
================================ */

.hero {
  position: relative;
  overflow: hidden;

  margin: 25px 60px 0;
  padding: 80px 70px;

  min-height: 430px;

  display: flex;
  align-items: center;
  justify-content: space-between;

  border-radius: 30px;

  background: linear-gradient(
    135deg,
    #1d4ed8,
    #2563eb,
    #60a5fa
  );

  color: white;

  box-shadow:
    0 20px 40px rgba(37, 99, 235, 0.25);
}

.hero-content {
  max-width: 650px;
  position: relative;
  z-index: 2;
}

.badge {
  display: inline-block;

  padding: 8px 15px;
  margin-bottom: 20px;

  border-radius: 30px;

  background: rgba(255, 255, 255, 0.2);

  font-size: 12px;
  font-weight: 700;

  letter-spacing: 1px;
}

.hero h1 {
  margin: 0;

  font-size: 48px;
  line-height: 1.1;

  font-weight: 800;
}

.hero h1 span {
  display: block;
  color: #dbeafe;
}

.hero-description {
  max-width: 520px;

  margin: 22px 0 30px;

  font-size: 16px;
  line-height: 1.7;

  color: #eff6ff;
}

/* BUTTON */

.btn {
  border: none;

  padding: 14px 25px;

  border-radius: 14px;

  background: white;
  color: #1d4ed8;

  font-size: 14px;
  font-weight: 700;

  cursor: pointer;

  transition: 0.2s;
}

.btn:hover {
  transform: translateY(-3px);

  box-shadow:
    0 10px 25px rgba(0, 0, 0, 0.15);
}

.btn span {
  margin-left: 8px;
  font-size: 18px;
}

/* HERO DECORATION */

.hero-decoration {
  width: 210px;
  height: 210px;

  display: flex;
  align-items: center;
  justify-content: center;

  border-radius: 50%;

  background: rgba(255, 255, 255, 0.15);

  font-size: 100px;

  transform: rotate(8deg);
}

/* ================================
   FEATURES
================================ */

.features {
  padding: 80px 60px;
}

.section-title {
  margin-bottom: 45px;
  text-align: center;
}

.section-title > span {
  font-size: 11px;
  font-weight: 800;

  letter-spacing: 2px;

  color: #2563eb;
}

.section-title h2 {
  margin-top: 8px;

  font-size: 30px;

  color: #172554;
}

.feature-container {
  max-width: 1050px;

  margin: auto;

  display: grid;

  grid-template-columns:
    repeat(3, 1fr);

  gap: 20px;
}

.feature {
  padding: 25px;

  display: flex;

  gap: 18px;

  background: rgba(255, 255, 255, 0.9);

  border: 1px solid #bfdbfe;

  border-radius: 20px;

  transition: 0.25s;

  box-shadow:
    0 8px 20px
    rgba(37, 99, 235, 0.08);
}

.feature:hover {
  transform: translateY(-6px);

  box-shadow:
    0 15px 30px
    rgba(37, 99, 235, 0.18);
}

/* ICON */

.icon {
  min-width: 48px;
  height: 48px;

  display: flex;
  align-items: center;
  justify-content: center;

  border-radius: 14px;

  font-size: 22px;
  font-weight: bold;

  background: #dbeafe;
  color: #2563eb;
}

.feature h3 {
  margin: 0 0 8px;

  font-size: 15px;

  color: #172554;
}

.feature p {
  margin: 0;

  color: #475569;

  font-size: 12px;

  line-height: 1.6;
}

/* ================================
   VIDEO
================================ */

.video-section {
  padding: 80px 60px;

  display: flex;

  align-items: center;

  justify-content: center;

  gap: 70px;

  background: rgba(239, 246, 255, 0.9);
}

.video-text {
  max-width: 400px;
}

.video-text > span {
  font-size: 11px;

  font-weight: 800;

  letter-spacing: 2px;

  color: #2563eb;
}

.video-text h2 {
  margin: 12px 0;

  font-size: 35px;

  line-height: 1.2;

  color: #172554;
}

.video-text strong {
  color: #2563eb;
}

.video-text p {
  color: #475569;

  line-height: 1.7;
}

.video-box {
  width: 500px;
}

.video-box video {
  width: 100%;

  display: block;

  border-radius: 20px;

  box-shadow:
    0 15px 35px
    rgba(37, 99, 235, 0.2);
}

/* ================================
   CTA
================================ */

.cta {
  margin: 70px 60px;

  padding: 45px 55px;

  display: flex;

  align-items: center;

  justify-content: space-between;

  border-radius: 25px;

  background: linear-gradient(
    135deg,
    #bfdbfe,
    #dbeafe
  );

  border: 1px solid #93c5fd;
}

.cta span {
  font-size: 11px;

  font-weight: 800;

  letter-spacing: 2px;

  color: #1d4ed8;
}

.cta h2 {
  margin: 8px 0 0;

  font-size: 27px;

  color: #172554;
}

.cta button {
  border: none;

  padding: 14px 22px;

  border-radius: 12px;

  background: #2563eb;

  color: white;

  font-weight: 700;

  cursor: pointer;

  transition: 0.2s;
}

.cta button:hover {
  transform: translateY(-3px);
}

/* ================================
   FOOTER
================================ */

footer {
  padding: 25px;

  text-align: center;

  color: #1e40af;

  font-size: 12px;
}

/* ================================
   RESPONSIVE
================================ */

@media (max-width: 900px) {

  .hero {
    margin: 20px;
    padding: 60px 35px;
  }

  .hero h1 {
    font-size: 38px;
  }

  .hero-decoration {
    display: none;
  }

  .features {
    padding: 60px 20px;
  }

  .feature-container {
    grid-template-columns: 1fr;
  }

  .video-section {
    padding: 60px 20px;

    flex-direction: column;

    gap: 30px;
  }

  .video-box {
    width: 100%;
  }

  .cta {
    margin: 40px 20px;

    padding: 35px 25px;

    flex-direction: column;

    align-items: flex-start;

    gap: 25px;
  }

}

</style>