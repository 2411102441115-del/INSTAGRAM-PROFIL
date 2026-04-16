## Pertanyaan README

### 1. jelaskan keputusan grid-cols/gap di tiap breakpoint - kenapa begitu
- **Mobile (default, `grid-cols-1`)**: layar kecil → feed dibuat 1 kolom agar gambar tetap jelas dan tidak terlalu kecil.
- **Tablet (`md:grid-cols-3`)**: layar medium sudah cukup luas → grid 3 kolom memberikan keseimbangan antara jumlah foto dan ukuran tiap foto.
- **Desktop (`lg:grid-cols-4`)**: layar besar → lebih banyak kolom (4) agar pemanfaatan ruang lebih efisien, feed terlihat padat seperti Instagram asli.
- **Gap (`gap-2`)** dipilih kecil agar mirip tampilan feed Instagram yang rapat, tapi tetap ada jarak antar foto.

### 2. bagaimana kamu memanfaatan utility responsive tailwind untuk memecahkan masalah layout yang muncul di mobile 
- **Order (`md:order-1`, `md:order-2`)**: di mobile avatar muncul di atas bio agar fokus pertama ke foto profil; di layar lebih besar urutannya diubah agar bio di kiri, avatar di kanan.
- **Button sizing (`sm:`, `md:`)**: tombol Follow/Edit lebih kecil di mobile, lebih besar di tablet/desktop agar lebih proporsional.
- **Grid utilities (`grid-cols-…`)**: mengatur jumlah kolom sesuai lebar layar sehingga masalah “foto terlalu kecil di mobile” bisa dihindari.

### 3. jelaskan trade-off antara memakai banyak utility classes vs membuat Component CSS tersenfiri
- **Kelebihan Utility Classes**:
  - Cepat untuk prototyping.
  - Konsisten dengan sistem desain Tailwind.
  - Tidak perlu bikin CSS terpisah.
- **Kekurangan Utility Classes**:
  - Class HTML bisa jadi sangat panjang.
  - Sulit dibaca kalau proyek makin kompleks.
- **Kelebihan Component CSS**:
  - Kode lebih rapi, readable.
  - Mudah dipakai ulang di banyak tempat.
- **Kekurangan Component CSS**:
  - Butuh effort tambahan untuk maintain CSS custom.
  - Mengurangi manfaat utama Tailwind (utility-first, tanpa bikin CSS banyak).
