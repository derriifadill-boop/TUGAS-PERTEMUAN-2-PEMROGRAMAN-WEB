# Pertemuan 3 : Bootstrap 5 

Proyek ini adalah simulasi halaman profil Instagram untuk brand *Nepenthe Stylee*, dibuat menggunakan **HTML, CSS, dan Bootstrap 5**.  
Tujuan utama dari project ini adalah latihan membuat layout web responsif dengan grid system Bootstrap, komponen tab navigasi, dan utility classes.

---

## Struktur Halaman
1. **Header Profil** → Foto profil, nama, tombol interaksi (Follow/Message).  
2. **Statistik** → Jumlah postingan, followers, dan following.  
3. **Bio** → Deskripsi singkat brand.  
4. **Tab Navigasi** → Posts, Reels, Tagged.  
5. **Feed** → 12 gambar produk ditampilkan responsif.  
6. **Similar Accounts** → Rekomendasi akun brand lain.  
7. **Footer** → Informasi hak cipta.  

---

## Struktur Folder
project/
├── index.html
├── costum.css
└── img/
├── logo profil.jpg
├── baju.jpg
├── celana.jpg
├── hoodie.jpg
├── jaket.jpg
├── jersey.jpg
├── kaos kaki.jpg
├── sepatu.jpg
├── sweater.jpg
├── sweatpants.webp
├── topi.jpeg
├── vest.jpeg
├── work jaket.jpeg
├── miracle.jpg
├── chmb.jpg
└── prfc.jpg


---

## Dependensi
- [Bootstrap 5.3.3](https://getbootstrap.com/) (via CDN)  
- [Bootstrap Icons](https://icons.getbootstrap.com/) (via CDN)  

---

## Cara Menjalankan
1. Clone atau download repository.  
2. Pastikan struktur folder sesuai (`index.html`, `costum.css`, dan folder `img/`).  
3. Buka file `index.html` di browser (double click atau via Live Server di VS Code).  

---

## Fitur Utama
- Layout responsif menggunakan Bootstrap Grid (`col-`, `col-sm-`, `col-md-`, `col-lg-`).  
- Komponen Tab untuk navigasi **Posts/Reels/Tagged**.  
- Feed 12 gambar dengan **responsive images** (`.img-fluid`).  
- Avatar profil & akun mirip dengan **border-radius** dan `object-fit`.  
- Dark mode dengan background hitam dan teks putih/abu-abu.  
- Tombol interaksi (Follow, Message) dengan order responsif.  

---

## Latihan & Pertanyaan

**Mengapa memilih konfigurasi `col` tertentu untuk tiap breakpoint?**  
Agar feed terlihat seimbang di semua device. Mobile → `col-12` (1 kolom, mudah dibaca), Tablet → `col-sm-6` / `col-md-4` (2–3 kolom, lebih padat), Desktop → `col-lg-3` (4 kolom, mirip layout Instagram asli).  

**Bagaimana memastikan tombol Follow/Edit Profile tetap mudah dijangkau di mobile?**  
Dipakai class `order-` responsif. Di mobile tombol ditaruh berdekatan di bawah username agar jempol mudah menjangkau, sedangkan di desktop urutannya lebih fleksibel dan estetis.  

**Jika postingan bertambah jadi 50, apa potensi masalah dan bagaimana solusi gridmu mengatasinya?**  
Masalah: halaman jadi panjang & berat karena load semua gambar sekaligus.  
Solusi: tetap pakai grid Bootstrap agar layout otomatis rapih (baris baru dibuat otomatis), dan bisa ditambah **lazy loading** pada `<img>` atau pagination/tab tambahan agar performa tetap lancar.  

---