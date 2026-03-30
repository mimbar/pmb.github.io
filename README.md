# PMB Universitas Siliwangi — Landing Page

Landing page statis informasi **daftar ulang** Penerimaan Mahasiswa Baru (PMB) Universitas Siliwangi.  
Dibuat dengan HTML, CSS, dan JavaScript ringan. Siap deploy ke GitHub Pages.

---

## Struktur File

```
├── index.html   ← Halaman utama (layout, style, render logic)
├── data.js      ← DATA JALUR SELEKSI — edit di sini saja
└── README.md    ← Dokumentasi & template referensi
```

> **Prinsip utama:** Anda hanya perlu mengedit **`data.js`**.  
> File `index.html` tidak perlu diubah kecuali untuk logo, teks hero, atau link sosial media.

---

## Cara Mengelola Kartu Jalur Seleksi

Buka file **`data.js`**. Isinya berupa array `jalurSeleksi`.  
**Hanya jalur yang ada di dalam array inilah yang akan tampil di halaman.**

### Properti setiap jalur

| Properti    | Keterangan                                        |
|-------------|---------------------------------------------------|
| `nama`      | Nama jalur seleksi                                |
| `deskripsi` | Penjelasan singkat 1 kalimat                      |
| `status`    | Lihat tabel status di bawah                       |
| `informasi` | URL halaman pengumuman & panduan daftar ulang     |
| `daftar`    | URL portal / halaman daftar ulang                 |

### Status badge

| Nilai status      | Tampilan badge            |
|-------------------|---------------------------|
| `"Dibuka"`        | 🟢 Hijau — Dibuka         |
| `"Segera Dibuka"` | 🟡 Kuning — Segera Dibuka |
| `"Ditutup"`       | 🔴 Merah — Ditutup        |
| `"Informasi"`     | ⚪ Abu — Informasi         |

### Menambah jalur baru

Tambahkan objek baru di dalam array:

```js
{
    nama: "SNBP",
        deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang dinyatakan lolos melalui jalur SNBP.",
        status: "Segera Dibuka",
        informasi: "#",
        daftar: "#"
},

{
    nama: "SNBT",
        deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang dinyatakan lolos melalui jalur SNBT.",
    status: "Dibuka",
    informasi: "#",
    daftar: "#"
},

{
    nama: "Seleksi Mandiri Barat",
        deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang lolos melalui Seleksi Mandiri Barat.",
    status: "Segera Dibuka",
    informasi: "#",
    daftar: "#"
},

{
    nama: "Seleksi Mandiri Unsil",
        deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang lolos melalui Seleksi Mandiri Unsil.",
    status: "Informasi",
    informasi: "#",
    daftar: "#"
}
```

### Menghapus jalur

**Hapus objeknya dari array — jangan dikomentar.**  
Komentar JavaScript tetap terlihat di source code browser oleh siapa pun.

---

## Template Referensi `data.js`

### 4 jalur lengkap

```js
var jalurSeleksi = [

  {
    nama: "SNBP",
    deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang dinyatakan lolos melalui jalur SNBP.",
    status: "Dibuka",
    informasi: "#",
    daftar: "#"
  },

  {
    nama: "SNBT",
    deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang dinyatakan lolos melalui jalur SNBT.",
    status: "Dibuka",
    informasi: "#",
    daftar: "#"
  },

  {
    nama: "Seleksi Mandiri Barat",
    deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang lolos melalui Seleksi Mandiri Barat.",
    status: "Segera Dibuka",
    informasi: "#",
    daftar: "#"
  },

  {
    nama: "Seleksi Mandiri Unsil",
    deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang lolos melalui Seleksi Mandiri Unsil.",
    status: "Informasi",
    informasi: "#",
    daftar: "#"
  }

];
```

### Hanya 1 jalur (SNBP)

```js
var jalurSeleksi = [

  {
    nama: "SNBP",
    deskripsi: "Informasi dan panduan daftar ulang bagi calon mahasiswa yang dinyatakan lolos melalui jalur SNBP.",
    status: "Dibuka",
    informasi: "#",
    daftar: "#"
  }

];
```

---

## Hal Lain yang Bisa Diedit di `index.html`

| Bagian            | Cari komentar ini di HTML          |
|-------------------|------------------------------------|
| Logo kampus       | `LOGO: Ganti src`                  |
| Favicon           | `FAVICON`                          |
| Judul hero        | `JUDUL UTAMA`                      |
| Subjudul hero     | `SUBJUDUL`                         |
| Catatan informasi | `CATATAN INFORMASI`                |
| Link Facebook     | `FACEBOOK`                         |
| Link Instagram    | `INSTAGRAM`                        |
| Email             | `EMAIL`                            |
| Warna identitas   | CSS Variables di `:root`           |

---

## Deploy ke GitHub Pages

1. Push semua file (`index.html`, `data.js`) ke repository.
2. Buka **Settings → Pages**.
3. Pilih branch `main` dan folder `/ (root)`.
4. Simpan — halaman aktif di `https://<username>.github.io/<repo>/`.
