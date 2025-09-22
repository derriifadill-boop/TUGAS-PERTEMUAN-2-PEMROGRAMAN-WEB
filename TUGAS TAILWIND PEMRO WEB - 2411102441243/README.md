# Instagram Profile Clone - Nepenthe Stylee (Tailwind CSS)

Proyek ini adalah simulasi halaman profil Instagram untuk brand *Nepenthe Stylee*, dibuat menggunakan **HTML, Tailwind CSS, dan Alpine.js**.  
Tujuan project ini adalah latihan membuat layout web responsif dengan pendekatan **utility-first** menggunakan Tailwind.

---

## Struktur Halaman
1. **Header Profil** → Foto profil, nama akun, tombol interaksi (Follow / Edit Profile).  
2. **Statistik** → Jumlah posting, followers, dan following.  
3. **Bio** → Deskripsi singkat brand.  
4. **Navigasi Tabs** → Posts, Reels, Tagged.  
5. **Feed** → 12 gambar produk ditampilkan responsif.  
6. **Footer** → Informasi hak cipta.  

---

## Struktur Folder
project/
├── index.html
└── img/
├── logo profil.jpg
├── post1.jpg
├── post2.jpg
├── ...
└── post12.jpg

markdown
Salin kode

---

## Dependensi
- [Tailwind CSS](https://tailwindcss.com/) (via CDN)  
- [Alpine.js](https://alpinejs.dev/) (via CDN, untuk navigasi tab)  
- Folder `img/` untuk resource gambar profil & posting  

---

## Cara Menjalankan
1. Clone atau download repository.  
2. Pastikan semua file gambar ada di folder `img/`.  
3. Buka `index.html` langsung di browser (atau gunakan Live Server di VS Code).  

---

## Penjelasan Desain

Desain halaman ini meniru struktur **profil Instagram** dengan pendekatan **mobile-first** dari Tailwind CSS.  

1. **Layout Responsif (Grid & Breakpoint)**  
   - Mobile → `grid-cols-1`: setiap posting full-width, mudah dibaca di layar kecil.  
   - Tablet → `sm:grid-cols-2 md:grid-cols-3`: lebih padat tapi masih jelas.  
   - Desktop → `lg:grid-cols-4`: mirip feed IG, efisien di layar besar.  
   - `gap-2` menjaga jarak konsisten antar foto.  

2. **Header Profil**  
   - Dibagi `grid-cols-3 md:grid-cols-4`.  
   - Avatar: `w-24 h-24 md:w-36 md:h-36` → ukuran otomatis sesuai device.  
   - Tombol **Follow/Edit Profile** pakai `order-1 md:order-2` → mudah dijangkau di mobile, lebih rapih di desktop.  

3. **Statistik & Bio**  
   - Statistik: `grid grid-cols-3 text-center` biar tiap angka proporsional.  
   - Bio pakai `text-sm` di mobile dan naik ke `md:text-base` untuk layar lebih besar.  

4. **Navigasi Tabs (Posts/Reels/Tagged)**  
   - `flex justify-center` untuk sejajar.  
   - Alpine.js (`x-data`, `x-show`) untuk logika pergantian tab.  
   - Class dinamis `:class` memberi highlight pada tab aktif.  

5. **Feed Foto (Posts)**  
   - `w-full h-60 object-cover` menjaga rasio dan cropping foto.  
   - Grid otomatis membuat baris baru bila postingan bertambah.  

6. **Footer**  
   - Minimalis dengan `text-gray-500 text-sm text-center`.  

---

## Pertanyaan Reflektif

**1. Jelaskan keputusan grid-cols/gap di tiap breakpoint — kenapa begitu?**  
- Mobile → 1 kolom agar konten jelas & fokus.  
- Tablet → 2–3 kolom untuk memanfaatkan layar lebih lebar.  
- Desktop → 4 kolom agar rapih dan mirip Instagram asli.  
- Gap `2` menjaga visual tetap lega dan konsisten antar gambar.  

**2. Bagaimana memanfaatkan utility responsive Tailwind untuk memecahkan masalah layout di mobile?**  
Dengan utility `sm:`, `md:`, `lg:` → avatar mengecil di mobile (`w-24`), tombol berpindah posisi (`order-1 md:order-2`), teks menyesuaikan (`text-sm md:text-base`).  
Hasilnya: pengalaman pengguna tetap nyaman di layar kecil maupun besar.  

**3. Jelaskan trade-off antara memakai banyak utility classes vs membuat component CSS tersendiri.**  
- **Utility classes:** cepat, fleksibel, langsung responsif. Tapi HTML jadi "ramai" penuh class.  
- **Component CSS:** HTML lebih bersih & reusable, tapi kurang fleksibel untuk variasi kecil atau kondisi responsif.  
Solusi: gabungkan keduanya. Pakai utility untuk layout, buat component CSS jika ada pola berulang.  

---

## Soal Latihan
- **Deskripsi Singkat:** Membuat halaman profil Instagram clone dengan Tailwind CSS.  
- **Ketentuan Wajib:** Header Profil, Bio, Feed minimal 12 gambar, Footer, penggunaan minimal 3 fitur responsif Tailwind (`grid-cols`, `order`, `gap`, dsb).  
- **Deliverables:**  
  1. File `index.html`  
  2. Folder `img/` berisi gambar profil & posting.  