<script setup>
import { ref } from 'vue'

const nama = ref('')
const email = ref('')
const pesan = ref('')

const kirimPesan = () => {
  if (!nama.value || !email.value || !pesan.value) {
    alert('Silakan isi semua data terlebih dahulu!')
    return
  }

  alert(`Terima kasih ${nama.value}! Pesan kamu berhasil dikirim.`)

  nama.value = ''
  email.value = ''
  pesan.value = ''
}
</script>


<template>
  <div class="contact-page">

    <!-- =========================
         HERO
    ========================== -->

    <section class="contact-hero">

      <div class="hero-content">

        <span class="hero-badge">
          💬 CONTACT US
        </span>

        <h1>
          Hubungi Kami
        </h1>

        <p>
          Ada pertanyaan atau butuh bantuan?
          Jangan ragu untuk menghubungi kami.
        </p>

      </div>

      <div class="hero-decoration">
        💙
      </div>

    </section>


    <!-- =========================
         CONTACT CONTENT
    ========================== -->

    <section class="contact-content">

      <!-- INFO KONTAK -->

      <div class="contact-info">

        <span class="section-label">
          GET IN TOUCH
        </span>

        <h2>
          Yuk, ngobrol<br />
          <span>bersama kami!</span>
        </h2>

        <p class="info-description">
          Kami siap membantu menjawab pertanyaan
          seputar produk, pemesanan, maupun layanan
          School Store.
        </p>


        <!-- ALAMAT -->

        <div class="info-item">

          <div class="info-icon">
            📍
          </div>

          <div>
            <h3>
              Alamat
            </h3>

            <p>
              Jl. Pendidikan No. 1,
              Soreang, Kab. Bandung
            </p>
          </div>

        </div>


        <!-- TELEPON -->

        <div class="info-item">

          <div class="info-icon">
            📞
          </div>

          <div>
            <h3>
              Telepon
            </h3>

            <p>
              (022) 123 4567
            </p>
          </div>

        </div>


        <!-- EMAIL -->

        <div class="info-item">

          <div class="info-icon">
            ✉️
          </div>

          <div>
            <h3>
              Email
            </h3>

            <p>
              info@smkyadikasoreang.sch.id
            </p>
          </div>

        </div>

      </div>


      <!-- =========================
           FORM
      ========================== -->

      <div class="contact-form-card">

        <div class="form-header">

          <span>
            SEND MESSAGE
          </span>

          <h2>
            Kirim Pesan ✨
          </h2>

          <p>
            Isi formulir di bawah dan kami akan
            segera menghubungi kamu.
          </p>

        </div>


        <form @submit.prevent="kirimPesan">

          <!-- NAMA -->

          <div class="form-group">

            <label>
              Nama
            </label>

            <input
              v-model="nama"
              type="text"
              placeholder="Masukkan nama kamu"
            />

          </div>


          <!-- EMAIL -->

          <div class="form-group">

            <label>
              Email
            </label>

            <input
              v-model="email"
              type="email"
              placeholder="Masukkan email kamu"
            />

          </div>


          <!-- PESAN -->

          <div class="form-group">

            <label>
              Pesan
            </label>

            <textarea
              v-model="pesan"
              rows="5"
              placeholder="Tulis pesan kamu di sini..."
            ></textarea>

          </div>


          <!-- BUTTON -->

          <button
            type="submit"
            class="send-button"
          >
            Kirim Pesan
            <span>→</span>
          </button>

        </form>

      </div>

    </section>


    <!-- =========================
         BOTTOM CARD
    ========================== -->

    <section class="help-section">

      <div class="help-icon">
        💙
      </div>

      <div>

        <h2>
          Butuh bantuan?
        </h2>

        <p>
          Tim School Store siap membantu kamu.
          Jangan sungkan untuk bertanya!
        </p>

      </div>

      <div class="help-decoration">
        ✦
      </div>

    </section>


    <!-- =========================
         FOOTER
    ========================== -->

    <footer>

      <div class="footer-logo">
        BlueShop
      </div>

      <p>
        © 2026 BlueShop. Made for students.
      </p>

    </footer>

  </div>
</template>


<style scoped>

/* =================================
   GLOBAL
================================= */

* {
  box-sizing: border-box;
  font-family:
    'Segoe UI',
    Arial,
    sans-serif;
}

.contact-page {
  min-height: 100vh;

  background:
    linear-gradient(
      180deg,
      #f0f9ff 0%,
      #ffffff 45%,
      #f0f9ff 100%
    );

  color: #1e3a5f;
}


/* =================================
   HERO
================================= */

.contact-hero {
  position: relative;

  overflow: hidden;

  max-width: 1250px;

  min-height: 300px;

  margin: 0 auto;

  padding: 60px 70px;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 0 0 35px 35px;

  background:
    linear-gradient(
      135deg,
      #60a5fa,
      #38bdf8,
      #2563eb
    );

  color: white;

  text-align: center;

  box-shadow:
    0 15px 40px
    rgba(37, 99, 235, 0.18);
}

.hero-content {
  position: relative;

  z-index: 2;

  max-width: 700px;
}

.hero-badge {
  display: inline-block;

  padding: 8px 16px;

  margin-bottom: 15px;

  border-radius: 30px;

  background:
    rgba(255, 255, 255, 0.2);

  border:
    1px solid
    rgba(255, 255, 255, 0.3);

  font-size: 12px;

  font-weight: 700;

  letter-spacing: 2px;
}

.contact-hero h1 {
  margin: 0 0 12px;

  font-size: 48px;

  font-weight: 800;
}

.contact-hero p {
  margin: 0;

  font-size: 16px;

  line-height: 1.6;

  color: #e0f2fe;
}

.hero-decoration {
  position: absolute;

  right: 80px;

  bottom: -35px;

  width: 150px;

  height: 150px;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 50%;

  background:
    rgba(255, 255, 255, 0.1);

  font-size: 75px;

  transform: rotate(-10deg);
}


/* =================================
   CONTACT CONTENT
================================= */

.contact-content {
  max-width: 1100px;

  margin: 70px auto;

  padding: 0 25px;

  display: grid;

  grid-template-columns:
    1fr 1fr;

  gap: 70px;

  align-items: start;
}


/* =================================
   CONTACT INFO
================================= */

.contact-info {
  padding-top: 15px;
}

.section-label {
  color: #0284c7;

  font-size: 11px;

  font-weight: 800;

  letter-spacing: 2px;
}

.contact-info h2 {
  margin: 12px 0;

  color: #173b5e;

  font-size: 38px;

  line-height: 1.2;
}

.contact-info h2 span {
  color: #38bdf8;
}

.info-description {
  max-width: 450px;

  margin-bottom: 35px;

  color: #64748b;

  font-size: 14px;

  line-height: 1.8;
}


/* =================================
   INFO ITEM
================================= */

.info-item {
  display: flex;

  align-items: center;

  gap: 17px;

  margin-bottom: 23px;

  padding: 15px;

  border-radius: 16px;

  transition: 0.25s;
}

.info-item:hover {
  background: #e0f2fe;

  transform: translateX(5px);
}

.info-icon {
  width: 48px;

  height: 48px;

  flex-shrink: 0;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 14px;

  background: #dff4ff;

  font-size: 21px;

  box-shadow:
    0 5px 15px
    rgba(14, 165, 233, 0.12);
}

.info-item h3 {
  margin: 0 0 5px;

  color: #2563eb;

  font-size: 15px;
}

.info-item p {
  margin: 0;

  color: #64748b;

  font-size: 13px;

  line-height: 1.5;
}


/* =================================
   FORM CARD
================================= */

.contact-form-card {
  padding: 35px;

  border:
    1px solid
    #dbeafe;

  border-radius: 25px;

  background:
    rgba(255, 255, 255, 0.9);

  box-shadow:
    0 15px 40px
    rgba(14, 165, 233, 0.1);
}

.form-header {
  margin-bottom: 25px;
}

.form-header span {
  color: #0284c7;

  font-size: 10px;

  font-weight: 800;

  letter-spacing: 2px;
}

.form-header h2 {
  margin: 7px 0;

  color: #173b5e;

  font-size: 28px;
}

.form-header p {
  margin: 0;

  color: #64748b;

  font-size: 13px;

  line-height: 1.6;
}


/* =================================
   FORM
================================= */

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;

  margin-bottom: 8px;

  color: #315a7d;

  font-size: 13px;

  font-weight: 700;
}

.form-group input,
.form-group textarea {
  width: 100%;

  padding: 13px 15px;

  border:
    1px solid
    #cbdff0;

  border-radius: 12px;

  outline: none;

  background: #f8fcff;

  color: #1e3a5f;

  font-size: 13px;

  transition: 0.2s;
}

.form-group input::placeholder,
.form-group textarea::placeholder {
  color: #94a3b8;
}

.form-group input:focus,
.form-group textarea:focus {
  border-color: #38bdf8;

  background: white;

  box-shadow:
    0 0 0 4px
    rgba(56, 189, 248, 0.12);
}

.form-group textarea {
  resize: vertical;

  min-height: 120px;
}


/* =================================
   SEND BUTTON
================================= */

.send-button {
  width: 100%;

  padding: 14px 20px;

  border: none;

  border-radius: 13px;

  background:
    linear-gradient(
      135deg,
      #38bdf8,
      #2563eb
    );

  color: white;

  font-size: 14px;

  font-weight: 700;

  cursor: pointer;

  box-shadow:
    0 8px 20px
    rgba(37, 99, 235, 0.2);

  transition: 0.25s;
}

.send-button span {
  margin-left: 8px;

  font-size: 17px;
}

.send-button:hover {
  transform: translateY(-3px);

  box-shadow:
    0 12px 25px
    rgba(37, 99, 235, 0.3);
}


/* =================================
   HELP SECTION
================================= */

.help-section {
  position: relative;

  overflow: hidden;

  max-width: 1050px;

  margin: 0 auto 70px;

  padding: 30px 35px;

  display: flex;

  align-items: center;

  gap: 20px;

  border-radius: 22px;

  background:
    linear-gradient(
      135deg,
      #e0f7ff,
      #dbeafe
    );

  border:
    1px solid #bae6fd;
}

.help-icon {
  width: 55px;

  height: 55px;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 16px;

  background: white;

  font-size: 25px;

  box-shadow:
    0 5px 15px
    rgba(37, 99, 235, 0.1);
}

.help-section h2 {
  margin: 0 0 5px;

  color: #1e40af;

  font-size: 19px;
}

.help-section p {
  margin: 0;

  color: #52708c;

  font-size: 13px;
}

.help-decoration {
  position: absolute;

  right: 35px;

  font-size: 55px;

  color: #7dd3fc;

  transform: rotate(15deg);
}


/* =================================
   FOOTER
================================= */

footer {
  padding: 35px 20px;

  text-align: center;

  background: #e0f2fe;

  border-top:
    1px solid #bae6fd;
}

.footer-logo {
  margin-bottom: 8px;

  color: #2563eb;

  font-family: Georgia, serif;

  font-size: 24px;

  font-weight: bold;
}

footer p {
  margin: 0;

  color: #64748b;

  font-size: 12px;
}


/* =================================
   RESPONSIVE
================================= */

@media (max-width: 800px) {

  .contact-hero {
    margin: 0 15px;

    min-height: 280px;

    padding: 50px 25px;
  }

  .contact-hero h1 {
    font-size: 38px;
  }

  .hero-decoration {
    display: none;
  }

  .contact-content {
    grid-template-columns: 1fr;

    gap: 40px;

    margin-top: 50px;
  }

  .contact-info h2 {
    font-size: 32px;
  }

  .help-section {
    margin: 0 20px 50px;

    padding: 25px;
  }

  .help-decoration {
    display: none;
  }

}


@media (max-width: 500px) {

  .contact-hero {
    border-radius: 0 0 25px 25px;
  }

  .contact-hero h1 {
    font-size: 32px;
  }

  .contact-hero p {
    font-size: 14px;
  }

  .contact-content {
    padding: 0 18px;
  }

  .contact-form-card {
    padding: 25px 20px;
  }

  .contact-info h2 {
    font-size: 28px;
  }

}
.contact-page {
  min-height: 100vh;

  background:
    linear-gradient(
      180deg,
      #f0f9ff 0%,
      #ffffff 45%,
      #f0f9ff 100%
    );

  color: #1e3a5f;
}

</style>