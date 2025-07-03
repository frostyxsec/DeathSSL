# DeathSSL Xposed Module

![DeathSSL Demo](https://raw.githubusercontent.com/frostyxsec/DeathSSL/refs/heads/main/demo_deathssl.png)

**DeathSSL** adalah module Xposed yang dirancang untuk **menonaktifkan SSL Pinning** pada aplikasi Android. Dengan modul ini, pengguna dapat melakukan intercept dan debugging traffic HTTPS menggunakan tools seperti **Burp Suite**, **Charles Proxy**, atau **Wireshark**, meskipun aplikasi target menggunakan SSL Pinning.

> ⚠️ **PERINGATAN**: Penggunaan module ini hanya diperbolehkan untuk keperluan **pengujian keamanan**, **pentesting aplikasi milik sendiri**, atau **penelitian edukatif**. Penggunaan untuk tujuan jahat melanggar hukum dan etika.

---

## 🔧 Fitur

- Bypass SSL Pinning pada berbagai metode umum
- Kompatibel dengan sebagian besar aplikasi Android
- Tidak memerlukan patch aplikasi target
- Ringan dan mudah diaktifkan melalui Xposed Installer

---

## 📦 Instalasi

### Persyaratan

- Perangkat Android dengan akses **root**
- **Xposed Framework** terinstal
- Android 5.0+ (Lollipop ke atas)

### Langkah-langkah

1. Unduh `deathssl.apk` dari [releases](#)
2. Instal APK:
   ```bash
   adb install deathssl.apk
   ```
3. Buka aplikasi **Xposed / LSposed Installer**
4. Aktifkan modul **DeathSSL**
5. Masuk ke pengaturan, aktifkan module untuk system dan target apk
6. Reboot perangkat

---

## 📋 Cara Penggunaan

1. Pastikan modul sudah aktif dan perangkat telah direboot.
2. Jalankan aplikasi target.
3. Pastikan proxy Anda (Burp, Charles, dsb.) sudah berjalan.
4. Atur proxy wifi
5. SSL Pinning pada aplikasi target akan dilewati, memungkinkan intercept HTTPS.

![DeathSSL in Action](https://raw.githubusercontent.com/frostyxsec/DeathSSL/refs/heads/main/testing.png)

---

## 🛠 Kompatibilitas

Telah diuji pada:

* Android 8 - 13
* Beberapa aplikasi banking, e-commerce, dan sosial media
* Emulator (Genymotion, AVD)

Catatan: Beberapa aplikasi mungkin masih menggunakan teknik proteksi tambahan seperti **TrustManager custom** atau proteksi dari framework seperti **OkHttp CertificatePinner**.

---

## ❗ Disclaimer

* Penulis tidak bertanggung jawab atas penyalahgunaan modul ini.
* Gunakan hanya pada aplikasi yang Anda miliki atau dengan izin eksplisit.
* Pelanggaran dapat mengakibatkan konsekuensi hukum.

---

## 📃 Lisensi

MIT License

---
