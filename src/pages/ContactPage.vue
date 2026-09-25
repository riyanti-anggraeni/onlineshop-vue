<template>
  <div class="contact-page">

    
    <section class="banner">
      <h1>Hubungi Kami</h1>
    </section>

    
    <section class="content">

      
      <div class="info">
        <h2>Info Kontak</h2>

        <div class="info-item">
          <h4>📍 Alamat</h4>
          <p>Jl. Pendidikan No. 1, Soreang, Kab. Bandung</p>
        </div>

        <div class="info-item">
          <h4>📞 Telepon</h4>
          <p>(022) 123 4567</p>
        </div>

        <div class="info-item">
          <h4>✉ Email</h4>
          <p>info@smkyadikasoreang.sch.id</p>
        </div>
      </div>

      
      <div class="form">
        <h2>Kirim Pesan</h2>

        <label>Nama</label>
        <input type="text" placeholder="Nama kamu">

        <label>Email</label>
        <input type="email" placeholder="Email kamu">

        <label>Pesan</label>
        <textarea placeholder="Tulis pesan kamu..."></textarea>

        <button>Kirim</button>
      </div>

    </section>

    
    <footer>
      © 2025 SMK Yadika Soreang — OnlineShop Soreang
    </footer>

  </div>
</template>

<style scoped>

* {
  box-sizing: border-box;
}

.contact-page {
  font-family: Arial, sans-serif;
  color: #58758c;
  min-height: 100vh;
}


.navbar {
  width: 70%;
  margin: auto;
  height: 70px;

  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  font-size: 14px;
  font-weight: bold;
}

.menu {
  display: flex;
  gap: 25px;
}

.menu a {
  text-decoration: none;
  color: #333;
  font-size: 13px;
}

.menu .active {
  color: #2878bd;
  border-bottom: 2px solid #2878bd;
  padding-bottom: 5px;
}


.banner {
  width: 70%;
  height: 125px;
  margin: auto;

  background: #285a9e;

  display: flex;
  justify-content: center;
  align-items: center;
}

.banner h1 {
  color: white;
  font-size: 27px;
}


.content {
  width: 70%;
  margin: 45px auto;

  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
}

.content h2 {
  font-size: 22px;
  margin-bottom: 25px;
}


.info-item {
  margin-bottom: 25px;
}

.info-item h4 {
  font-size: 13px;
  margin-bottom: 6px;
}

.info-item p {
  font-size: 12px;
  color: #777;
}


.form {
  display: flex;
  flex-direction: column;
}

.form label {
  font-size: 12px;
  font-weight: bold;
  margin-bottom: 7px;
}

.form input,
.form textarea {
  border: none;
  border-bottom: 1px solid #ccc;
  padding: 10px 5px;
  margin-bottom: 25px;
  outline: none;
  font-size: 12px;
}

.form textarea {
  height: 70px;
  resize: none;
}

.form button {
  width: 80px;
  padding: 10px;

  border: none;
  border-radius: 20px;

  background: #3c8ed9;
  color: white;

  cursor: pointer;
}


footer {
  width: 70%;
  margin: 70px auto 0;
  padding: 20px;

  text-align: center;
  border-top: 1px solid #ddd;

  font-size: 11px;
  color: #777;
}

</style>