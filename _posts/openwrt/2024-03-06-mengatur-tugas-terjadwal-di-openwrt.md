---
layout: page
sidebar: left
subheadline: Scheduled Tasks
title:  "Mengatur Tugas Terjadwal di OpenWrt"
teaser: "setting scheduled tasks openwrt."
breadcrumb: true
tags:
    - openwrt
categories:
    - openwrt
header: false
---
### Table of Contents
*  Auto generated table of contents
{:toc}

OpenWrt adalah sistem operasi sumber terbuka untuk perangkat jaringan, seperti router. Salah satu fitur yang berguna dari OpenWrt adalah kemampuannya untuk menjalankan tugas terjadwal. Dengan mengatur tugas terjadwal, Anda dapat mengotomatiskan berbagai tugas, seperti mem-backup konfigurasi, memperbarui perangkat lunak, atau menjalankan skrip tertentu pada waktu yang ditentukan.

<a href="https://shope.ee/AUWHzCfxKa" target="_blank"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgpbULz3IUJfJ5bmJFaSCX7xGRZ-ghSiiN9rIUK8GtFT8hA09YYtqaHSFonXJEVO8yMu4tKPdnjozs2thxUOF96uBCJsrqG9-Nc23EkrztW0inoAgkyI52ZADPWR79FT4WPcMap91PiCFVgsGuKk7xBrfxBWvrC9jV_7GGtIhD_Zy5krYpyHI7iKNGClGZL/s320/no_markReactNative-snapshot-image_13.png" width="320" height="320"></a>

Berikut adalah langkah-langkah untuk membuat dan mengatur tugas terjadwal di OpenWrt:

## Langkah 1: Menginstal Paket Cron

Pertama, pastikan paket cron telah diinstal di perangkat OpenWrt Anda. Anda dapat melakukannya dengan menjalankan perintah berikut di terminal:

```bash
opkg update
opkg install cron
```

<a href="https://shope.ee/AUWHzCfxKa" target="_blank"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgpbULz3IUJfJ5bmJFaSCX7xGRZ-ghSiiN9rIUK8GtFT8hA09YYtqaHSFonXJEVO8yMu4tKPdnjozs2thxUOF96uBCJsrqG9-Nc23EkrztW0inoAgkyI52ZADPWR79FT4WPcMap91PiCFVgsGuKk7xBrfxBWvrC9jV_7GGtIhD_Zy5krYpyHI7iKNGClGZL/s320/no_markReactNative-snapshot-image_13.png" width="320" height="320"></a>

## Langkah 2: Konfigurasi Cron

Setelah menginstal paket cron, Anda perlu mengkonfigurasi file cron untuk menambahkan tugas-tugas yang ingin Anda jalankan secara terjadwal. File konfigurasi cron terletak di `/etc/crontabs/root`.

```bash
vi /etc/crontabs/root
```

Tambahkan baris-baris berikut untuk menentukan waktu dan perintah yang ingin Anda jalankan:

```bash
# Menjalankan perintah setiap jam pada menit ke-30
30 * * * * perintah_anda_di_sini

# Menjalankan perintah setiap hari pada pukul 2:00 pagi
0 2 * * * perintah_anda_di_sini

# Menjalankan perintah setiap hari Minggu pada pukul 4:30 pagi
30 4 * * 0 perintah_anda_di_sini
```

<a href="https://shope.ee/AUWHzCfxKa" target="_blank"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgpbULz3IUJfJ5bmJFaSCX7xGRZ-ghSiiN9rIUK8GtFT8hA09YYtqaHSFonXJEVO8yMu4tKPdnjozs2thxUOF96uBCJsrqG9-Nc23EkrztW0inoAgkyI52ZADPWR79FT4WPcMap91PiCFVgsGuKk7xBrfxBWvrC9jV_7GGtIhD_Zy5krYpyHI7iKNGClGZL/s320/no_markReactNative-snapshot-image_13.png" width="320" height="320"></a>

## Langkah 3: Memuat Ulang Cron

Setelah menyimpan perubahan pada file cron, pastikan untuk memuat ulang daemon cron agar perubahan tersebut berlaku:

```bash
/etc/init.d/cron reload
```

## Catatan Penting:

- Pastikan untuk memberikan perintah yang lengkap dan benar. Contoh, jika Anda ingin menjalankan skrip bash, pastikan untuk menyertakan jalur lengkap ke skrip tersebut (misalnya `/usr/bin/myscript.sh`).
- Selalu uji coba tugas terjadwal Anda dengan menambahkan tugas sederhana terlebih dahulu dan memeriksa apakah mereka dijalankan sesuai jadwal yang ditentukan.

<a href="https://shope.ee/AUWHzCfxKa" target="_blank"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgpbULz3IUJfJ5bmJFaSCX7xGRZ-ghSiiN9rIUK8GtFT8hA09YYtqaHSFonXJEVO8yMu4tKPdnjozs2thxUOF96uBCJsrqG9-Nc23EkrztW0inoAgkyI52ZADPWR79FT4WPcMap91PiCFVgsGuKk7xBrfxBWvrC9jV_7GGtIhD_Zy5krYpyHI7iKNGClGZL/s320/no_markReactNative-snapshot-image_13.png" width="320" height="320"></a>

Dengan mengikuti langkah-langkah di atas, Anda dapat dengan mudah mengatur dan menjalankan tugas terjadwal di perangkat OpenWrt Anda sesuai kebutuhan.

## Simak tutorial openwrt lainnya
{: .t60 }
{% include list-posts tag='openwrt' %}