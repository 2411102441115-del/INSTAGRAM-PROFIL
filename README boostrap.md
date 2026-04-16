# pertanyaan README

## 1. jelaskan keputusan grid-cols/gap di tiap breakpoint - kenapa begitu
Pemilihan konfigurasi kolom untuk setiap breakpoint dilakukan agar tampilan konten tetap proporsional dan nyaman dilihat pada berbagai ukuran layar:
- **Mobile (≤576px, `col-12`)**  
  Foto ditampilkan penuh 1 kolom agar tidak terlalu kecil dan tetap jelas.
- **Tablet (≥768px, `col-md-4`)**  
  Ditampilkan dalam 3 kolom (3 × 4 = 12) sehingga ruang layar lebih efisien tanpa mengurangi keterbacaan.
- **Desktop (≥992px, `col-lg-3` atau `col-lg-2`)**  
  Jumlah kolom dapat ditambah (4–6 kolom) agar pengguna dapat melihat lebih banyak foto sekaligus.

tampilan feed akan selalu responsif, konsisten, dan nyaman diakses di semua perangkat.

## 2. bagaimana kamu memastikan tombol follow/edit profil tetap mudah dijangkau di mobile?jelaskan pendekatannya
Agar tombol tetap mudah digunakan pada layar kecil:
- Menggunakan **utility class Bootstrap** (`order-*`, `text-center`, `mt-3`) sehingga tombol berpindah ke bawah bio pada layar mobile.
- Tombol diberi ukuran **`btn-sm`** agar proporsional dengan layar kecil.
- Jarak antar tombol diatur menggunakan **gap** agar tidak berhimpitan.

Dengan pendekatan ini, tombol selalu terlihat jelas, mudah ditekan, dan tetap berada pada posisi yang mudah dijangkau oleh jempol di perangkat mobile.


## 3. jika postingan bertambah jadi 50 apa potensi masalah dan bagaimana solusi gridmu mengatasinya?
Jika jumlah postingan meningkat hingga 50:
- **Masalah potensial:**
  - Halaman menjadi terlalu panjang (scrolling berlebihan).
  - Performa menurun karena banyak gambar dimuat sekaligus.
- **Solusi grid Bootstrap:**
  Grid akan otomatis melakukan **wrap** ke baris berikutnya sehingga tata letak tetap rapi.
  Optimasi tambahan:
    - **Lazy loading** (`loading="lazy"`) pada gambar.
    - Menambahkan **pagination** atau **infinite scroll**.
    - Optimasi ukuran file gambar agar lebih ringan.

Dengan solusi ini, feed tetap responsif, rapi, dan performa aplikasi tidak terganggu meskipun jumlah postingan bertambah banyak.
