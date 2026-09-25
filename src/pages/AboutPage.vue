<template>
    <main class="about-page">
        <h1>TENTANG KAMI</h1>
    </main>

    <main class="cerita">
        <section class="cerita-text">
            <h1>Cerita Kita</h1>

            <p>
                online shop ini di kelola oleh siswa/i smk yadika jurusan PPLG
                sebagai proyek sekaligus membant teman teman mendapatkan
                perlengkapan sekolah dengan mudah dan terjangkau.
            </p>
            <p>
                setiap produk dipilih dengan dikurasi tim kecil siswa,
                dengan mengambil langsung di koperasi sekolah.
            </p>
        </section>

        <section class="image">
            <div class="cerita-image">
                <h1>FOTO</h1>
            </div>
        </section>
    </main>
    </template>

    <style scoped>
    .about-page {
        text-align: center;
        padding: 2rem;
        background: linear-gradient(rgb(39, 153, 241), rgb(51, 144, 231));
        border-radius: 5px;
        margin-bottom: 20px;
        

    }
    
    .cerita {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 70%;
        margin: auto;
        gap: 30px;
    }

    .cerita-text {
        flex: 1;
        
    }
    .cerita-text h1 {
        
        margin-bottom: 30px;
    }

    .cerita-text p{
        margin-bottom: 30px;
        line-height: 20px;
    }

    .image {
        display: flex;
        justify-content: center;
        align-items: center;
        flex: 1;
        min-height: 150px;
        padding: 2rem;
        text-align: center;
        box-sizing: border-box;
        background: linear-gradient(rgb(39, 153, 241), rgb(51, 144, 231));
        border-radius: 10px;
        box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.1);
    }

    .cerita-image {
        display: flex;
        justify-content: center;
        justify-items:center;
        align-items: center;
    }
</style>

