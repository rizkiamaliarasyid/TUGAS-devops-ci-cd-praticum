# Laporan Praktikum Pertemuan 02: Git Advanced - Branching Strategies

**Nama:** Rizki Amalia Rasyid Ridha  
**NIM:** 105841121223  
**Kelas/Mata Kuliah:** [Nama Kelas Anda]  

---

## 🌿 Task 1: Implementasi GitFlow

Pada praktikum ini, saya telah mengimplementasikan alur kerja **GitFlow** pada repositori lokal dan remote. Berikut adalah tahapan yang dilakukan:
1. Melakukan inisialisasi repositori dengan struktur GitFlow (`main` dan `develop`).

2. Membuat *feature branch* baru untuk mengembangkan fitur spesifik.
3. Melakukan *commit* perubahan pada *feature branch*.
4. Menggabungkan (*merge*) fitur yang sudah selesai kembali ke branch `develop`.
5. Membuat *release branch* sebagai persiapan sebelum rilis ke *production*.
6. Melakukan *merge* dari *release branch* ke `main` (sebagai rilis final) dan juga kembali ke `develop` agar tersinkronisasi.

*(Screenshot riwayat branch GitFlow)*
![GitFlow Branches](screenshots/gitflow-branches.png)

---

## ⚔️ Task 2: Resolve Merge Conflicts

### Dokumentasi Proses Resolusi Konflik
Konflik penggabungan (*merge conflict*) sengaja dibuat dan diselesaikan dengan langkah-langkah berikut:

1. **Terjadinya Konflik:** Konflik terjadi ketika saya mencoba melakukan *merge* dua *branch* yang memodifikasi baris kode yang sama pada file yang sama. Git menghentikan proses *merge* otomatis dan menandai file tersebut sebagai *unmerged*.
2. **Mengidentifikasi Konflik:** Saya membuka file yang bermasalah. Git menandai area konflik dengan indikator `<<<<<<< HEAD`, `=======`, dan `>>>>>>> [nama-branch]`.
3. **Resolusi Manual:** - Saya menghapus penanda konflik dari Git.
   - Saya menentukan kode mana yang akan dipertahankan (apakah perubahan dari *current branch*, *incoming branch*, atau gabungan keduanya).
4. **Penyelesaian:** Setelah file diperbaiki dan disimpan, saya menjalankan `git add [nama-file]` untuk menandai bahwa konflik telah diselesaikan, lalu menjalankan `git commit` untuk menyelesaikan proses *merge*.

*(Screenshot proses atau hasil resolusi konflik di VS Code/Terminal)*
![Merge Conflict Resolution](screenshots/merge-conflict-resolution.png)