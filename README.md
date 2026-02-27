# Portfolio Website 


---

## Tampilan Setiap Section / Fitur

### Navbar
Navigasi di bagian atas halaman berisi link ke Home, About Me, dan Certificates. Responsive dengan hamburger menu di tampilan mobile menggunakan Bootstrap.

### Section Home
Berisi foto profil, nama, tagline sebagai Mahasiswa, deskripsi singkat, dan dua tombol CTA (Tentang Saya & Sertifikat).

### Section About Me
Berisi foto, deskripsi diri, skills dengan progress bar, dan pengalaman.

### Section Certificates
Berisi 3 kartu sertifikat dalam layout grid. Setiap kartu menampilkan judul, penerbit, tahun, dan deskripsi singkat.

### Footer
Berisi teks copyright di bagian bawah halaman dengan background warna ungu.

---

## Penjelasan Code Setiap Section / Fitur

### Navbar
```html
<nav class="navbar navbar-expand-lg bg-body-tertiary sticky-top">
  <div class="container">
    <a class="navbar-brand" href="#home">Nama Kamu</a>
    <button class="navbar-toggler" ...>
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav ms-auto">
        <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
        ...
      </ul>
    </div>
  </div>
</nav>
```

Menggunakan komponen navbar Bootstrap 5 dengan `sticky-top` agar selalu tampil di atas halaman. `navbar-expand-lg` membuat navbar collapse di layar kecil dan menampilkan hamburger menu. 
Navbar merupakan bagian navigasi utama yang berada di bagian atas halaman website. Pada website ini, navbar dibuat menggunakan komponen bawaan Bootstrap 5 dengan class navbar dan navbar-expand-lg. Class tersebut memungkinkan navbar tampil dalam bentuk horizontal pada layar besar, namun berubah menjadi hamburger menu pada layar kecil (responsive).
Penggunaan sticky-top membuat navbar tetap berada di bagian atas layar saat pengguna melakukan scroll. Dengan demikian, navigasi tetap mudah diakses kapan saja tanpa harus kembali ke atas halaman.
Di dalam navbar terdapat container yang berfungsi untuk membatasi lebar konten agar tetap rapi dan tidak terlalu melebar pada layar besar. Menu navigasi seperti Home, About Me, dan Certificates dibuat menggunakan list <ul> dan <li>, lalu diratakan ke kanan menggunakan class ms-auto.
Hamburger menu bekerja menggunakan fitur collapse Bootstrap yang membutuhkan file JavaScript Bootstrap agar dapat membuka dan menutup menu secara otomatis di tampilan mobile.

### Section Home
```html
<section id="home" class="text-center py-5 section-home">
  <div class="container">
    <img src="..." alt="Foto Profil" class="foto-profil rounded-circle mb-4">
    <h1 class="fw-bold">Nama Kamu</h1>
    <p class="fs-5 text-secondary">UI/UX Designer</p>
    <a href="#about" class="btn btn-ungu">Tentang Saya</a>
  </div>
</section>
```
Menggunakan Bootstrap utility class `text-center`, `py-5`, `fw-bold`, `fs-5`. Class `foto-profil` dan `btn-ungu` adalah class custom dari `style.css`.
Section Home merupakan bagian pertama yang dilihat oleh pengunjung saat membuka website. Section ini berfungsi sebagai perkenalan singkat atau hero section.

Class text-center digunakan untuk meratakan seluruh teks ke tengah, sehingga tampilan terlihat lebih fokus dan simetris. Class py-5 memberikan padding atas dan bawah agar konten tidak terlalu mepet dengan tepi layar.

Foto profil menggunakan class rounded-circle sehingga gambar tampil dalam bentuk lingkaran. Biasanya ditambahkan custom CSS seperti object-fit: cover agar gambar tetap proporsional dan tidak terlihat gepeng.

Nama ditampilkan menggunakan heading dengan class fw-bold untuk mempertegas identitas. Tagline menggunakan fs-5 dan text-secondary agar terlihat lebih ringan dan tidak terlalu dominan dibanding nama.

Terdapat tombol CTA (Call To Action) yang dibuat menggunakan class btn dari Bootstrap serta class custom seperti btn-ungu untuk memberikan warna identitas. Tombol ini mengarahkan pengguna ke bagian About atau Certificates.

### Section About Me - Skills
```html
<p class="mb-1">Figma</p>
<div class="progress mb-3">
  <div class="progress-bar" role="progressbar"
    style="width: 90%;" aria-valuenow="90"
    aria-valuemin="0" aria-valuemax="100">90%
  </div>
</div>
```
Menggunakan komponen Progress Bar dari Bootstrap 5. Lebar bar diatur langsung lewat `style="width: 90%"`. Atribut `aria-valuenow`, `aria-valuemin`, `aria-valuemax` dipakai untuk aksesibilitas.
Skill ditampilkan menggunakan komponen progress dari Bootstrap. Di dalamnya terdapat progress-bar yang lebarnya diatur menggunakan style="width: 90%" untuk menunjukkan tingkat penguasaan suatu skill.

Atribut aria-valuenow, aria-valuemin, dan aria-valuemax digunakan untuk meningkatkan aksesibilitas, terutama bagi pengguna screen reader. Dengan cara ini, website tetap ramah bagi pengguna dengan kebutuhan khusus.

Progress bar ini memanfaatkan sistem flex dan CSS bawaan Bootstrap sehingga tampil konsisten tanpa perlu banyak styling tambahan.
### Section About Me - Pengalaman

```html
<ul>
  <li class="mb-2"><strong>2023 - Sekarang</strong> — UI/UX Designer di Creative Studio</li>
  <li class="mb-2"><strong>2022 - 2023</strong> — Junior Designer di Digital Agency XYZ</li>
  <li class="mb-2"><strong>2021 - 2022</strong> — Design Intern di Startup ABC</li>
</ul>
```
Daftar pengalaman menggunakan list HTML biasa dengan tag `<ul>` dan `<li>`.
Bagian pengalaman dibuat menggunakan list HTML (<ul> dan <li>). Setiap item pengalaman diberi class mb-2 untuk memberikan jarak antar baris agar lebih rapi.

Penggunaan tag <strong> pada tahun membuat bagian waktu terlihat lebih tegas dan mudah dibaca. Struktur sederhana ini menjaga tampilan tetap clean dan profesional.

### Section Certificates
```html
<div class="row g-4">
  <div class="col-12 col-sm-6 col-lg-4 d-flex">
    <div class="card h-100 w-100 shadow-sm">
      <div class="card-body d-flex flex-column">
        <h5 class="card-title">Google UX Design Certificate</h5>
        <p class="card-text text-secondary flex-grow-1">...</p>
        <a href="#" class="btn btn-ungu mt-3">Lihat Sertifikat</a>
      </div>
    </div>
  </div>
</div>
```
Grid Bootstrap `col-12 col-sm-6 col-lg-4` membuat layout 1 kolom (mobile), 2 kolom (tablet), 3 kolom (desktop). `h-100` membuat semua card setinggi kolom. `flex-grow-1` mendorong tombol ke bawah card.
Section Certificates menampilkan sertifikat dalam bentuk card menggunakan sistem grid Bootstrap.

Class row digunakan sebagai pembungkus kolom, sedangkan g-4 memberikan jarak antar card. Kombinasi class col-12 col-sm-6 col-lg-4 membuat layout menjadi responsif:

1 kolom pada mobile

2 kolom pada tablet

3 kolom pada desktop

Setiap sertifikat menggunakan komponen card Bootstrap yang memberikan tampilan kotak dengan bayangan (shadow-sm). Class h-100 memastikan semua card memiliki tinggi yang sama agar terlihat sejajar.

Di dalam card, digunakan d-flex flex-column untuk mengatur tata letak secara vertikal. Class flex-grow-1 pada deskripsi membuat tombol selalu berada di bagian bawah card meskipun panjang teks berbeda-beda.

Pendekatan ini membuat tampilan lebih rapi dan konsisten.
---

Footer terletak di bagian paling bawah halaman dan berisi informasi copyright. Biasanya menggunakan class text-center agar teks berada di tengah, serta padding seperti py-3 untuk memberi ruang.

Background ungu dibuat menggunakan custom CSS agar sesuai dengan identitas warna website. Sementara itu, text-white memastikan teks tetap terbaca dengan kontras yang baik.

Footer berfungsi sebagai penutup halaman sekaligus memperkuat branding visual website.

## Teknologi yang Digunakan

| Teknologi | Kegunaan |
|---|---|
| HTML5 | Struktur halaman |
| CSS3 | Styling custom (warna, layout, font) |
| Bootstrap 5 | Navbar, grid system, card, progress bar, responsive design |
