# Laman Web YATI (Fasa 1)

Laman statik dwibahasa (BM/EN) untuk Yayasan Pendidikan Teknologi dan Insani (YATI).
Tiada proses *build*: Vercel terus menghidangkan `index.html` dan folder `assets/`.

## Struktur

```
index.html            Keseluruhan laman (BM dan EN dalam fail yang sama)
assets/yati-emblem.png    Lambang YATI (header dan hero)
assets/yati-logo-full.png Logo penuh (imej pratonton pautan media sosial)
assets/favicon.png        Ikon tab pelayar
```

Setiap teks ditulis dua kali: `<span class="ms">…</span>` untuk BM dan `<span class="en">…</span>` untuk English.
Untuk mengemas kini kandungan, ubah kedua-dua span.

## Pelancaran ke Vercel

1. Cipta repositori GitHub baharu (cth. `yati-website`) dan muat naik semua fail dalam folder ini.
2. Di vercel.com: **Add New → Project**, pilih repositori tersebut. Framework Preset: **Other**. Tekan **Deploy**.
3. Semak laman di alamat sementara `*.vercel.app`.
4. Di Vercel: **Project → Settings → Domains**, tambah `yayasanyati.net` dan `www.yayasanyati.net`.

## Tetapan DNS di Squarespace Domains (hanya selepas langkah 4)

| Tindakan | Jenis | Nama | Nilai |
|---|---|---|---|
| Padam | A | @ | 198.49.23.144, 198.49.23.145, 198.185.159.144, 198.185.159.145 (preset "Squarespace Defaults") |
| Tambah | A | @ | `76.76.21.21` (atau nilai yang dipaparkan Vercel) |
| Tambah/ubah | CNAME | www | `cname.vercel-dns.com` (atau nilai yang dipaparkan Vercel) |

**Jangan ubah:** nameserver, rekod MX (`smtp.google.com`), rekod TXT SPF, dan tetapan DNSSEC. E-mel `yatiadmin@yayasanyati.net` akan terus berfungsi.

## Perkara untuk dikemas kini kemudian

- Nombor akaun Bank Islam (bahagian "Cara Menyumbang", cari `Akan dimaklumkan`).
- Nombor pendaftaran pemerbadanan Akta 258 sebaik sijil dikeluarkan.
