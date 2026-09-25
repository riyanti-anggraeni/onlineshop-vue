<template>
  <section class="about-page">

    <!-- HEADER -->
    <div class="about-header">

      <span class="badge">
        🏫 TENTANG KAMI
      </span>

      <h1>
        Tentang <span>Onlineshop Sekolah</span>
      </h1>

      <p>
        Kenali lebih dekat Onlineshop SMK Yadika Soreang,
        tempat belanja kebutuhan sekolah dengan mudah dan nyaman.
      </p>

    </div>


    <!-- ABOUT CONTENT -->
    <div class="about-content">

      <!-- CARD SEKOLAH -->
      <div class="about-card">

        <div class="icon">
          🏫
        </div>

        <h2>
          SMK Yadika Soreang
        </h2>

        <p>
          SMK Yadika Soreang merupakan sekolah yang berfokus
          pada pendidikan vokasi dan pengembangan keterampilan
          siswa agar siap menghadapi dunia kerja maupun melanjutkan
          pendidikan.
        </p>

      </div>


      <!-- CARD ONLINE SHOP -->
      <div class="about-card">

        <div class="icon">
          🛒
        </div>

        <h2>
          Onlineshop Sekolah
        </h2>

        <p>
          Onlineshop Sekolah dibuat untuk memudahkan siswa dan
          warga sekolah dalam membeli berbagai kebutuhan sekolah,
          seperti pakaian, atribut, dan perlengkapan lainnya.
        </p>

      </div>


      <!-- CARD TUJUAN -->
      <div class="about-card">

        <div class="icon">
          🎯
        </div>

        <h2>
          Tujuan Kami
        </h2>

        <p>
          Memberikan pengalaman belanja yang mudah, cepat,
          praktis, dan nyaman bagi seluruh warga sekolah.
        </p>

      </div>

    </div>


    <!-- KEUNGGULAN -->
    <div class="keunggulan">

      <h2>
        Kenapa Belanja di Sini?
      </h2>

      <div class="features">

        <!-- FEATURE 1 -->
        <div class="feature">

          <div class="feature-icon">
            ⚡
          </div>

          <h3>
            Praktis
          </h3>

          <p>
            Pesan kebutuhan sekolah tanpa harus datang langsung.
          </p>

        </div>


        <!-- FEATURE 2 -->
        <div class="feature">

          <div class="feature-icon">
            💰
          </div>

          <h3>
            Harga Terjangkau
          </h3>

          <p>
            Produk sekolah dengan harga yang ramah untuk siswa.
          </p>

        </div>


        <!-- FEATURE 3 -->
        <div class="feature">

          <div class="feature-icon">
            📦
          </div>

          <h3>
            Produk Berkualitas
          </h3>

          <p>
            Menyediakan produk sekolah yang nyaman dan berkualitas.
          </p>

        </div>


        <!-- FEATURE 4 -->
        <div class="feature">

          <div class="feature-icon">
            😊
          </div>

          <h3>
            Mudah Digunakan
          </h3>

          <p>
            Tampilan sederhana sehingga mudah digunakan semua orang.
          </p>

        </div>

      </div>

    </div>

  </section>
</template>


<style scoped>

/* ================================
   HALAMAN ABOUT
================================ */

.about-page {

  min-height: 100vh;

  padding: 60px 60px 100px;

  background:
    linear-gradient(
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

.about-header {

  max-width: 750px;

  margin: 0 auto 50px;

  text-align: center;
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
    0 8px 20px
    rgba(37, 99, 235, 0.25);
}


.about-header h1 {

  margin: 10px 0 15px;

  font-size: 42px;

  font-weight: 800;

  color: #172554;

}


.about-header h1 span {

  color: #2563eb;

}


.about-header p {

  margin: 0;

  color: #475569;

  font-size: 15px;

  line-height: 1.7;

}


/* ================================
   ABOUT CARD
================================ */

.about-content {

  max-width: 1100px;

  margin: auto;

  display: grid;

  grid-template-columns:
    repeat(3, 1fr);

  gap: 25px;

}


.about-card {

  padding: 30px;

  text-align: center;

  background: white;

  border: 1px solid #bfdbfe;

  border-radius: 22px;

  box-shadow:
    0 10px 25px
    rgba(37, 99, 235, 0.10);

  transition: 0.3s ease;

}


.about-card:hover {

  transform: translateY(-8px);

  box-shadow:
    0 18px 35px
    rgba(37, 99, 235, 0.20);

}


/* ================================
   ICON
================================ */

.icon {

  width: 70px;

  height: 70px;

  margin: 0 auto 20px;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 50%;

  background: #dbeafe;

  font-size: 32px;

  box-shadow:
    0 6px 15px
    rgba(37, 99, 235, 0.12);

}


.about-card h2 {

  margin: 0 0 12px;

  color: #172554;

  font-size: 20px;

}


.about-card p {

  margin: 0;

  color: #64748b;

  font-size: 14px;

  line-height: 1.7;

}


/* ================================
   KEUNGGULAN
================================ */

.keunggulan {

  max-width: 1100px;

  margin: 60px auto 0;

  padding: 40px;

  background: rgba(255, 255, 255, 0.9);

  border: 1px solid #bfdbfe;

  border-radius: 25px;

  box-shadow:
    0 10px 25px
    rgba(37, 99, 235, 0.10);

}


.keunggulan > h2 {

  margin: 0 0 35px;

  text-align: center;

  color: #172554;

  font-size: 28px;

}


/* ================================
   FEATURES
================================ */

.features {

  display: grid;

  grid-template-columns:
    repeat(4, 1fr);

  gap: 20px;

}


.feature {

  padding: 20px;

  text-align: center;

  border-radius: 18px;

  transition: 0.3s ease;

}


.feature:hover {

  background: #eff6ff;

  transform: translateY(-5px);

}


.feature-icon {

  width: 60px;

  height: 60px;

  margin: 0 auto 15px;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 18px;

  background: #dbeafe;

  font-size: 30px;

}


.feature h3 {

  margin: 0 0 8px;

  color: #2563eb;

  font-size: 17px;

}


.feature p {

  margin: 0;

  color: #64748b;

  font-size: 13px;

  line-height: 1.6;

}


/* ================================
   RESPONSIVE
================================ */

@media (max-width: 900px) {

  .about-page {

    padding: 50px 25px 80px;

  }


  .about-content {

    grid-template-columns: 1fr;

  }


  .features {

    grid-template-columns:
      repeat(2, 1fr);

  }

}


@media (max-width: 600px) {

  .about-page {

    padding: 40px 20px 60px;

  }


  .about-header h1 {

    font-size: 30px;

  }


  .features {

    grid-template-columns: 1fr;

  }


  .keunggulan {

    padding: 25px 15px;

  }

}

</style>