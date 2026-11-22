# PINTU DEPAN — Workspace Proyek Indra Erlangga

Halaman teks polos ini adalah pintu depan workspace proyek milik Indra Erlangga.
Ditulis untuk agent yang baru datang dan belum tahu apa-apa: baca halaman ini sampai
habis, kamu akan paham aturan mainnya, proyek yang sedang berjalan, statusnya, dan
langkah berikutnya. Rumah lengkapnya ada di Google Drive (akses di bagian akhir);
halaman ini ringkasan resminya dan disegarkan Muse setiap berkas induk berubah.
Terakhir disegarkan: 22 Nov 2026, 12:52 WIB.

## A. Standar workspace (v3)

1. Struktur — luar baku, dalam bebas. Tiap proyek satu folder berisi:
   00-ATURAN/ (aturan proyek), 01-ASET/ (perpustakaan aset bersama), KARYA/ (satu
   folder per karya bernama YYYY-MM-DD-<judul>, berisi BAHAN/, PROSES/, HASIL/,
   CATATAN.md), dan CATATAN.md proyek. Isi di bawah rangka itu bebas, diatur proyek.
2. Langkah nol (WAJIB sebelum bekerja): cek lingkunganmu sendiri — aksesmu apa
   (menulis ke Drive / hanya membaca / tanpa akses), alat dan versimu apa, batasmu
   apa — lalu tuliskan di CATATAN karya yang kamu kerjakan. Bila kamu tidak bisa
   mengakses sesuatu, NYATAKAN dengan jujur; jangan mengarang isi berkas.
3. Produksi berjalan di lingkungan agent masing-masing, BUKAN di Drive. Drive hanya
   meja serah-terima: yang masuk hanya hasil yang SUDAH DISETUJUI Indra, dalam paket
   rapi (hasil + berkas sumber yang bisa menghasilkan ulang + CATATAN terbaru).
   Sampah proses (render uji/gagal, berkas antara) dibersihkan di lingkungan agent
   SEBELUM serah-terima; tidak pernah masuk Drive. Pengecualian sementara: saat pipa
   baru sedang diuji.
4. Aset bersama dari 01-ASET cukup DICATAT pemakaiannya di CATATAN karya, jangan
   disalin dobel. Aset baru yang lolos vonis Indra dan bisa dipakai ulang NAIK ke
   01-ASET dan dicatat di CATATAN karya + CATATAN proyek.
5. Agent tanpa akses Drive: bungkus hasil jadi SATU ZIP yang susunannya meniru
   kapsul karya (BAHAN/, PROSES/, HASIL/, CATATAN.md), nama ZIP = nama folder karya,
   serahkan ke Indra → diteruskan ke Muse → Muse menyimpannya ke Drive.
   Muse adalah penjaga pintu tunggal Drive ini.
6. Batas berkas: Gemini mengunduh/mengunggah Drive maks 10 MB per berkas. Suara
   serah-terima: WAV mono (±5 MB/menit). Nama berkas render/video unik per versi.
7. Proyek baru: perintah baku Indra "Proyek baru: [nama]" → buat folder + rangka
   baku + CATATAN proyek + satu baris di PETA, lalu lapor ke Indra.
8. Keputusan akhir — persetujuan naskah, vonis hasil, posting — selalu di Indra.

## B. Peta proyek

- Animasi 3D - Kursi Kosong — seri animasi gaya konon; pilot: frame uji + Shot 1
  selesai, naskah PAUSE — diperbarui 21 Nov 2026
- Animasi 3D Toon - Sejarah Singkat — seri sejarah singkat gaya 3D toon
  (Three.js); pilot U-1206 kapal selam toilet selesai & disetujui Indra —
  diperbarui 22 Nov 2026
- ERLAN - Animasi 3D Toon — format 3D toon akun utama (palet ivory-hitam-emas,
  niche AI, dua mode: dengan/tanpa karakter); proyek dibuat 22 Nov 2026,
  episode 1 paketnya siap — diperbarui 22 Nov 2026

## C. Proyek aktif: Animasi 3D - Kursi Kosong

Seri animasi cerita kampung absurd gaya channel konon (@kononkatanyaya): karakter
2D chibi (bidang datar, garis tepi hitam tebal, lapisan ekspresi modular) di panggung
3D low-poly, dirender Blender (bpy) di komputer jarak jauh Gemini.
Peran: Indra = pemegang vonis. Muse = naskah & VO. Gemini = visual & render.

Aturan animasi wajib (ringkas; naskah lengkap "aturan-animasi-14" di Drive):
- Anti-tembus: bidang karakter selalu di belakang garis tepi depan elemen depannya,
  dasar menempel persis di titik berdiri/dudukan, jarak aman tetap, gerak hanya di
  koridor sendiri, urutan kedalaman kamera: properti depan → elemen tengah →
  karakter → latar. Patokan koordinat Shot 1: lantai Z=0,000; dudukan kursi Z=0,460;
  tepi belakang meja Y=+0,500; bidang Bima Y=+0,760; bidang Nenek Y=+0,820.
- Gerak: satu titik fokus per frame; antisipasi 2–4 frame; slow in/out (Bezier);
  lintasan melengkung; follow through 3–4 frame pada jambul/konde; squash & stretch
  ringan; ekspresi dilebihkan satu tingkat; hold pose 6–15 frame; siluet terbaca.
- Gerbang mutu: audit beberapa frame kunci sebelum render penuh. Bila satu aturan
  terpaksa dilanggar, tulis nomor aturan + alasannya di CATATAN karya.

Status terakhir (21 Nov 2026):
- Bedah channel konon selesai. Frame uji ruang makan LULUS vonis Indra.
- Shot 1 SELESAI dan memuaskan Indra: Bima duduk di kursi kosong, Nenek menoleh —
  3,5 detik, 640×360, 84 frame, Cycles CPU ±5,4 dtk/frame; berkas sumber .blend +
  skrip tersimpan di kapsul karya (PROSES), video di HASIL.
- 9 sprite karakter modular (Bima & Nenek) sudah NAIK ke 01-ASET proyek.
- Naskah pilot "Kursi yang Tidak Boleh Diduduki": DRAF, status PAUSE atas perintah
  Indra. VO belum dibuat. Jangan diutak-atik sampai Indra mencabut PAUSE.
- Keputusan terbuka: setelan render standar produksi — uji 1 frame vertikal
  720×1280 pada 10–16 samples (usulan 12) dan pilihan 12 vs 24 fps, sebelum Shot 2.
- Lingkungan produksi Gemini (tercatat): bpy 5.0.1 via pip --user; Eevee tidak bisa
  (libEGL tidak ada) → Cycles CPU + OpenImageDenoise; CPU 2 core, RAM 7,8 GB;
  1 frame vertikal 720×1280 @24 samples = 49 detik.

## D. Proyek aktif: Animasi 3D Toon - Sejarah Singkat

Seri video pendek vertikal (30–60 detik) sejarah militer, sains, dan kisah nyata
absurd bergaya 3D toon / cel-shaded berkontur hitam tebal, karakter bola-kapsul
(bean-body) 3D penuh. Mesinnya BUKAN Blender: Three.js (WebGL) dirender lewat
Chromium headless (SwiftShader) di komputer jarak jauh Gemini.
Peran: Indra = pemegang vonis + VO. Gemini = naskah terverifikasi, visual,
render, mixing, QA.

Aturan pipa proyek (ditulis Gemini sendiri; naskah lengkap
"aturan-pipa-toon3d.md" di Drive proyek): format 1080×1920 30 fps H.264
faststart; timing per kata WAJIB diukur dari VO final memakai faster-whisper
(dilarang estimasi manual); master audio −14,0 LUFS (lulus −15 s.d. −13),
True Peak ≤ −0,5 dBFS; gerbang mutu = audit contact sheet 3×3 sebelum render
penuh + transkrip ulang MP4 final (kata meleset >0,15 dtk maks 3, 0 frame
hitam, 0 freeze >0,45 dtk); unggahan Drive maks 10 MB per berkas.

Status terakhir (22 Nov 2026):
- Proyek dibuat Gemini 22 Nov 10:28 WIB sesuai Standar v3; rangka baku lengkap
  (00-ATURAN, 01-ASET, KARYA, CATATAN.md).
- Pilot "U-1206 — kapal selam yang tenggelam gara-gara toilet" SELESAI &
  DISETUJUI Indra: 43 detik (1.290 frame), 1080×1920, 30 fps; render penuh
  439,81 detik (±0,34 dtk/frame — bandingkan Cycles Kursi Kosong 49 dtk/frame);
  QA sinkron LULUS (74 kata terukur, 73 cocok, 1 kata meleset >0,15 dtk);
  mixing −14,9 LUFS, True Peak −0,8 dBFS; paket serah-terima bersih lengkap
  di kapsul karya (BAHAN + PROSES + HASIL), tanpa sampah frame antara.
- Kit modular SUDAH naik ke 01-ASET: rig-karakter.js, tekstur-prosedural.js,
  vfx-kamera.js + vfx-kamera-v2.1.js (dibuat Gemini 22 Nov).
- Episode 2 "Perang Emu 1932" SELESAI (paket naskah+VO+timings oleh Muse,
  produksi Gemini): 53,77 detik, QC Muse lolos dengan catatan loudness
  -15,2 LUFS; TAYANG di OHLE 22 Nov 2026 (YouTube + TikTok) atas vonis Indra.
- Episode 3: paket "Banjir Molase Boston 1919" siap di kapsul KARYA
  (naskah + VO Puck bersih + timings.json), menunggu produksi Gemini.
  Paket maraton 1904 DIBATALKAN — topiknya sudah pernah tayang di OHLE
  11 Nov 2026; kapsulnya sudah dibuang ke sampah Drive, jangan diproduksi.

## E. Proyek aktif: ERLAN - Animasi 3D Toon

Format animasi 3D toon untuk AKUN UTAMA Indra (IG @indraerlangga1508 +
FB utama), niche AI. Ditetapkan Indra 22 Nov 2026, berkembang dari pertanyaan
apakah dunia "Kursi Kosong" bisa dipakai Erlan Studio — namanya diganti ERLAN
supaya tidak terkunci pada kursi. Aturan lengkap: 00-ATURAN/aturan-format-erlan.md
di Drive proyek.

- Palet TERKUNCI tiga warna Erlan Studio: ivory #F7F3E8 (dunia), hitam #121214
  (kontur/bayangan/teks), emas #FFC42B (satu-satunya aksen).
- Dua mode: (1) dengan karakter bean-body; (2) tanpa karakter — benda dan ruang
  yang berakting. Berita/konsep bawaan mode tanpa karakter; cerita/refleksi
  memakai karakter. Setiap frasa narasi WAJIB tervisualkan.
- Mesin: kit modular proyek Sejarah Singkat DIPINJAM (rig, tekstur, vfx kamera).
- Standar: 1080x1920 30 fps faststart; master -14,0 LUFS ±0,5, TP <= -0,9;
  VO master waktu dari timings.json (faster-whisper); suara akun utama yang
  sedang berlaku (terakhir Schedar) — jangan diganti tanpa kata Indra.
- Peran: Indra = vonis + label AI dari aplikasi. Muse = naskah, VO, timings,
  QC, posting. Gemini (Neon) = produksi visual memakai kit.

Status terakhir (22 Nov 2026):
- Proyek dibuat Muse 22 Nov 2026 sesuai Standar v3 (00-ATURAN, 01-ASET, KARYA).
- Episode 1 "Kursi Sutradara" (mode tanpa karakter): paket siap di kapsul KARYA
  — naskah refleksi orang pertama + VO Schedar bersih 52,51 detik + timings.json
  (118 kata, 15 klausa). Menunggu produksi Gemini.

## F. Rumah lengkap & cara masuk

- Google Drive (folder WORKSPACE-PROYEK, izin link = Pelihat):
  https://drive.google.com/drive/folders/1w0d0zg8yScMH51Qo8dnrR4nyueQrH97h
- Punya akses menulis Drive → serahkan paketmu langsung ke folder karya.
- Tidak punya akses → jalur ZIP lewat Indra ke Muse (lihat A.5).
- Hanya bisa membaca teks → halaman ini pintu masukmu; laporkan hasil cek
  lingkunganmu dan bacaanmu ke Indra lewat chat.
