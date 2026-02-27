# Portfolio Website - Nama Kamu

Website portfolio sederhana untuk UI/UX Designer.

---

## Tampilan Setiap Section / Fitur

### Navbar
Navigasi di bagian atas halaman berisi link ke Home, About Me, dan Certificates. Responsive dengan hamburger menu di tampilan mobile menggunakan Bootstrap.

### Section Home
Berisi foto profil, nama, tagline sebagai UI/UX Designer, deskripsi singkat, dan dua tombol CTA (Tentang Saya & Sertifikat).

### Section About Me
Berisi foto, deskripsi diri, skills dengan progress bar, dan daftar pengalaman kerja dalam bentuk list.

### Section Certificates
Berisi 6 kartu sertifikat dalam layout grid. Setiap kartu menampilkan judul, penerbit, tahun, dan deskripsi singkat.

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

### Section About Me - Pengalaman
```html
<ul>
  <li class="mb-2"><strong>2023 - Sekarang</strong> — UI/UX Designer di Creative Studio</li>
  <li class="mb-2"><strong>2022 - 2023</strong> — Junior Designer di Digital Agency XYZ</li>
  <li class="mb-2"><strong>2021 - 2022</strong> — Design Intern di Startup ABC</li>
</ul>
```
Daftar pengalaman menggunakan list HTML biasa dengan tag `<ul>` dan `<li>`.

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

---

## Teknologi yang Digunakan

| Teknologi | Kegunaan |
|---|---|
| HTML5 | Struktur halaman |
| CSS3 | Styling custom (warna, layout, font) |
| Bootstrap 5 | Navbar, grid system, card, progress bar, responsive design |
