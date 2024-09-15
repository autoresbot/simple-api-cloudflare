[![Version](https://img.shields.io/badge/version-1.0.0-brightgreen)](https://github.com/autoresbot/simple-api-cloudflare/releases)

# Simple API Cloudflare

Selamat datang di **Simple API Cloudflare**! Ini adalah API sederhana yang dirancang untuk integrasi dengan **Cloudflare**. Proyek ini memanfaatkan **Node.js** dan **Express** untuk menyediakan endpoint API yang dapat digunakan untuk berbagai kebutuhan terkait Cloudflare.

## Fitur Utama

- **Pengelolaan DNS**: Tambahkan, hapus, dan perbarui catatan DNS menggunakan Cloudflare API.
- **Pengaturan Firewall**: Kelola aturan firewall untuk melindungi aplikasi Anda.
- **Statistik Penggunaan**: Akses statistik penggunaan dan performa aplikasi melalui Cloudflare.

## Prasyarat

Sebelum memulai, pastikan Anda telah menginstal **Node.js** dan **npm**. Anda juga memerlukan **Cloudflare API Token**.

- **Node.js**: Versi minimal 16.x
- **npm**: Versi minimal 8.x

## Instalasi

Ikuti langkah-langkah berikut untuk menginstal dan menjalankan aplikasi ini secara lokal:

1. **Clone repositori**:

   ```bash
   git clone https://github.com/autoresbot/simple-api-cloudflare.git
   ```

2. **Masuk ke direktori proyek**:

   ```bash
   cd simple-api-cloudflare
   ```

3. **Instal dependensi**:

   ```bash
   npm install
   ```

4. **Buat file konfigurasi**:

   Salin file `.env.example` ke `.env` dan sesuaikan nilai-nilai dengan lingkungan Anda. Pastikan untuk mengisi `CF_API_TOKEN` dengan token API Cloudflare Anda.

   ```bash
   cp .env.example .env
   ```

5. **Jalankan aplikasi**:

   ```bash
   npm start
   ```

## Penggunaan

API ini menyediakan beberapa endpoint yang dapat Anda akses. Berikut adalah beberapa contoh:

- **Menambahkan Catatan DNS**:

  ```http
  POST /api/dns
  ```

  - **Request Body**:

    ```json
    {
      "type": "A",
      "name": "example.com",
      "content": "192.0.2.1",
      "ttl": 3600
    }
    ```

- **Menghapus Catatan DNS**:

  ```http
  DELETE /api/dns/:id
  ```

- **Mengatur Aturan Firewall**:

  ```http
  POST /api/firewall
  ```

  - **Request Body**:

    ```json
    {
      "action": "allow",
      "ip": "192.0.2.1"
    }
    ```

## Dokumentasi

Untuk informasi lebih lanjut tentang endpoint API dan penggunaan, kunjungi [dokumentasi API Cloudflare](https://developers.cloudflare.com/api/).

## Kontribusi

Kami menyambut kontribusi dari siapa saja! Jika Anda ingin berkontribusi, harap ikuti langkah-langkah berikut:

1. Fork repositori ini.
2. Buat branch baru (`git checkout -b fitur-baru`).
3. Lakukan perubahan.
4. Commit perubahan Anda (`git commit -am 'Menambahkan fitur baru'`).
5. Push branch ke GitHub (`git push origin fitur-baru`).
6. Buat pull request.

## Lisensi

Proyek ini dilisensikan di bawah lisensi **MIT License** - lihat file [LICENSE](LICENSE) untuk detail lebih lanjut.

## Kontak

Jika Anda memiliki pertanyaan, jangan ragu untuk menghubungi kami di:

- **Email**: [autoresbot@gmail.com](mailto:autoresbot@gmail.com)
- **Website**: [autoresbot](https://autoresbot.com)

---

Terima kasih telah menggunakan **Simple API Cloudflare**! 😊
