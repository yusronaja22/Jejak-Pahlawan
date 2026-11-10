# Aturan Operasional & Protokol Instalasi Software (Antigravity)

Instruksi dan ketentuan ini berlaku untuk semua interaksi dalam proyek ini mengenai download, instalasi, konfigurasi, dan pemecahan masalah software/package/library/dependency.

## 1. Alur Kerja Instalasi & Akses Jaringan
1. **Pemeriksaan Lingkungan Awal**:
   - Selalu cek apakah tools/package manager yang diperlukan sudah terpasang.
   - Periksa konektivitas jaringan (Internet) sebelum mengunduh atau menginstal.
2. **Identifikasi Sandbox vs Bypass**:
   - Terminal default berjalan dalam *Standard Sandbox Mode* (terisolasi tanpa akses internet dan filesystem luar).
   - Untuk perintah yang membutuhkan internet atau instalasi global di Windows (misal `winget`, `npm install -g`, `git clone`, unduh installer resmi), gunakan `BypassSandbox: true`.
3. **Pemberitahuan & Persetujuan Permission**:
   - Jelaskan secara transparan kepada pengguna perintah apa yang akan dijalankan dan mengapa hak akses jaringan/sistem dibutuhkan.
4. **Package Manager yang Didukung**:
   - `winget` (Windows Package Manager resmi)
   - `npm` / `npx` (Node.js ecosystem)
   - `pip` / `python`
   - `git`
   - `choco` (Chocolatey)
   - `powershell` (script instalasi resmi seperti `.msi`, `.exe`, atau `.ps1`)
5. **Sumber Terpercaya**:
   - Hanya unduh file instalasi dari domain/situs resmi pengembang atau repositori terverifikasi (GitHub releases resmi, PyPI, npmjs, Microsoft Store/winget).
6. **Eksekusi & Konfigurasi Otomatis**:
   - Jalankan instalasi dan lakukan konfigurasi environment/PATH yang diperlukan setelah izin diberikan.
7. **Verifikasi Wajib**:
   - Selalu verifikasi instalasi dengan mengecek versi (`--version` atau `Get-Command`) atau menjalankan uji fungsi sederhana sebelum menyatakan instalasi sukses.
8. **Analisis Kegagalan & Solusi**:
   - Jika instalasi gagal, analisis kode error/output log dan berikan langkah penyelesaian yang jelas.

## 2. Ketentuan Keamanan
- **DILARANG** mengunduh aplikasi dari sumber yang tidak resmi atau meragukan.
- **DILARANG** menonaktifkan Windows Defender, firewall, atau antivirus.
- **DILARANG** mengubah pengaturan keamanan sistem tanpa persetujuan eksplisit dari pengguna.
- **DILARANG** menjalankan perintah berbahaya, script tidak dikenal, atau menghapus file sistem Windows.
- **DILARANG** mengklaim instalasi berhasil tanpa melakukan proses verifikasi langsung.

