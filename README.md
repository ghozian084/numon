# numon

**Jelajah Numon** — game edukasi matematika SMP berbasis lokasi (GPS + kamera/AR). Numon tersebar di sekitar sekolah; dekati, lihat lewat kamera, lalu tangkap dengan menjawab soal Aljabar, Geometri, Bilangan, atau Statistika.

Semua ada di satu file: `index.html` (tanpa build, tanpa server).

## Cara mencoba

- **Di komputer:** buka `index.html` di browser, pilih **Mode simulasi** (ketuk peta atau pakai tombol panah untuk berjalan).
- **Di HP dengan GPS & kamera:** halaman harus dibuka lewat **HTTPS**, misalnya dengan mengaktifkan GitHub Pages (Settings → Pages → branch ini, folder root).

## Fitur uji coba (baru)

| Fitur | Keterangan | Diatur di |
|---|---|---|
| Combo beruntun | Jawaban benar berturut-turut memberi bonus +5 s/d +20 poin; chip "Beruntun ×N" muncul di HUD | otomatis |
| Batas waktu | Bilah waktu di lembar soal; habis = Numon kabur. Jawab di paruh pertama waktu = bonus +5 | Atur → Batas waktu (0/20/30/60 dtk) |
| Petunjuk 50:50 | Menghapus 2 pilihan salah; poin tangkapan itu jadi setengah | Atur → Petunjuk per sesi (0/3/5) |
| Getar & suara | Umpan balik getar + nada saat benar/salah | Atur → Getar & suara |
| Riwayat jawaban | 8 jawaban terakhir di tab Koleksi, plus statistik "Beruntun terbaik" | Koleksi |
| Peta dunia nyata | Pilih **Jalan (OpenStreetMap)**, **Satelit** (Esri World Imagery), atau **Topografi** (gaya lama). Tombol +/− (atau scroll mouse) untuk zoom | Atur → Jenis peta |
| Ekspor CSV | Unduh semua jawaban (nama, materi, benar/salah, waktu, soal, kunci) untuk guru | Atur → Unduh riwayat jawaban |

Mode simulasi memakai lokasi GPS terakhir di perangkat; kalau belum pernah ada, game mencoba mengambil lokasi sekali, lalu jatuh ke Monas, Jakarta. Peta nyata butuh internet; kalau ubin peta gagal dimuat, grid 10 m tetap tampil.

Catatan: keluar dari layar AR saat soal sudah muncul dihitung sebagai jawaban salah, supaya siswa tidak bisa "ganti soal" dengan keluar-masuk.

Progres disimpan di `localStorage` perangkat masing-masing.
