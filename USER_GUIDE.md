# Panduan Admin: Cara Mengedit Konten Website KiknKleen

Panduan ini dibuat untuk membantu Anda mengedit teks (copywriting) dan gambar pada setiap bagian (section) di website KiknKleen. Semua konten utama berada di dalam satu file bernama `src/pages/index.astro`.

## 📂 Persiapan

1.  Buka project di Text Editor (VS Code).
2.  Buka file: **`src/pages/index.astro`**
3.  Gunakan fitur **Find** (`Ctrl + F` atau `Cmd + F`) untuk mencari bagian yang ingin diedit dengan cepat menggunakan kata kunci yang diberikan di bawah ini.

---

## 1. Bagian Hero (Halaman Utama Paling Atas)

Ini adalah bagian pertama yang dilihat pengunjung.

**Cari Kata Kunci:** `id="home"` atau `Outfit Udah 10/10`

### 📝 Edit Teks (Copywriting)
-   **Judul Utama (Headline):** Cari teks `Outfit Udah 10/10`. Ubah teks di dalam tag `<h1>...</h1>`.
    -   Gunakan `<br />` jika ingin memotong baris (Enter).
    -   Teks berwarna abu-abu ada di dalam `<span class="text-gray-400">...</span>`.
-   **Deskripsi (Sub-headline):** Cari teks `Jangan biarin sepatu kotor`. Ubah teks di dalam tag `<p>...</p>`.
-   **Tombol CTA:** Cari `Cuci Sekarang!`. Ubah teks dan link di `href="..."` (misal ke `#contact` atau link WhatsApp).
-   **Statistik:** Cari `500+` atau `Sepatu Dicuci` untuk mengubah angka dan label statistik di bawah tombol.

### 🖼️ Edit Gambar Hero
-   **Gambar Sepatu Utama:** Cari `alt="Nike Air Force 1 Floating"`.
    -   Ubah `src="/Nike.png"` dengan nama file gambar baru Anda.
    -   **Penting:** Pastikan file gambar baru sudah dimasukkan ke dalam folder `public/`.
    -   Contoh: Jika punya `sepatu-baru.png` di folder `public`, ubah jadi `src="/sepatu-baru.png"`.

---

## 2. Bagian Layanan (Services)

Bagian kartu-kartu yang menampilkan daftar harga dan jenis layanan.

**Cari Kata Kunci:** `id="services"` atau `Layanan Kami`

### 📝 Edit Teks & Harga
-   **Judul Seksi:** Cari `Perawatan Premium`.
-   **Kartu Layanan:** Cari nama layanan, misal `Layanan Cuci Sepatu`.
-   **Item & Harga:** Di bawah setiap judul layanan, ada daftar item.
    -   Cari nama paket (misal `Bersih Banget`).
    -   Cari harga (misal `40K`) di sebelahnya.
    -   Cari deskripsi kecil di bawahnya (misal `Bersihin ekstra, cocok buat...`).
-   Untuk menambah harga/item baru, copy-paste satu blok `<li>...</li>` dan edit isinya.

---

## 3. Bagian Tentang Kami (About)

Bagian yang menjelaskan keunggulan ("Why Choose Us").

**Cari Kata Kunci:** `id="about"` atau `Kenapa Pilih Kami` (atau cari teks `Kami Tahu Cara`)

### 📝 Edit Teks
-   **Judul:** Cari `Kami Tahu Cara`.
-   **Deskripsi:** Cari `Di KiknKleen sepatu atau tas nggak asal disikat`.
-   **Poin-poin Keunggulan:** Cari judul poin seperti `Ditangani Oleh Ahlinya`, `Premium Treatment`, dll. Edit judul dan deskripsi kecil di bawahnya.

### 🖼️ Edit Gambar
-   Bagian ini menggunakan gambar dari internet (Unsplash) atau folder public.
-   Cari tag `<img` di dalam bagian ini.
-   Ubah link di `src="..."` dengan link gambar baru atau path file lokal (misal `/foto-team.jpg` jika ada di folder `public`).

---

## 4. Bagian Before & After (Slider)

Bagian interaktif geser gambar sebelum dan sesudah cuci.

**Cari Kata Kunci:** `id="comparison-container"`

### 🖼️ Ganti Gambar Slider
-   **Gambar SUDAH Jadi (After):** Cari `id="after-img"`.
    -   Ubah `src="/after-shoe.png"` menjadi gambar sepatu bersih Anda.
-   **Gambar SEBELUM Jadi (Before):** Cari `id="before-img"`.
    -   Ubah `src="/before-shoe.png"` menjadi gambar sepatu kotor Anda.
-   **Tips:** Pastikan kedua gambar (Before dan After) memiliki **ukuran (dimensi) yang sama persis** agar slider pas.

---

## 5. Bagian Galeri (Portfolio)

Grid foto-foto hasil pengerjaan.

**Cari Kata Kunci:** `id="gallery"`

### 🖼️ Tambah/Ganti Foto
-   Cari baris kode `<img src="/Galeri/..."`.
-   Untuk mengganti: Ubah nama file di `src="..."`.
-   Untuk menambah foto baru:
    1.  Copy satu blok `div` pembungkus gambar (dari `<div class="break-inside-avoid...">` sampai penutup `</div>`).
    2.  Paste di bawah item terakhir.
    3.  Ganti `src` gambarnya dengan file baru di folder `public/Galeri/`.

---

## 6. Bagian Kontak & Footer

Formulir pemesanan dan informasi kontak di bawah.

**Cari Kata Kunci:** `id="contact"`

### 📝 Edit Kontak
-   **Nomor WhatsApp:** Cari link `https://wa.me/628138818306`. Ubah angkanya dengan nomor baru (format 628...). Jangan lupa ubah juga teks tampilan nomornya.
-   **Alamat:** Cari `Lokasi Workshop` atau `Bandung, Bojongloa Kaler`.
-   **Link Google Maps:** Cari `href="https://www.google.com/maps/search/..."`. Ganti dengan link Google Maps lokasi baru Anda.

### 📝 Edit Jam Operasional (di Footer)
-   Cari `Jam Operasional`.
-   Edit jampada teks `09:00 - 20:00 WIB` sesuai kebutuhan.

---

## 💡 Tips Penting
1.  **Backup:** Sebelum edit banyak, copy dulu isi file `index.astro` ke file lain (misal `index-backup.txt`) biar aman.
2.  **Gambar:** Selalu taruh gambar baru di folder `public`. Jika di dalam folder `public` ada folder `Galeri`, maka aksesnya `/Galeri/nama-file.jpg`.
3.  **Simpan:** Tekan `Ctrl + S` (Windows) atau `Cmd + S` (Mac) untuk menyimpan perubahan. Website biasanya akan refresh otomatis di browser jika sedang dijalankan (`npm run dev`).
