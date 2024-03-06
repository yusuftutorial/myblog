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

<center><a href="https://shope.ee/7fC6foRbmb" target="_blank"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEi6th-GjZI-0MAlsFc8uy07oAHeAYfwgPYPc9KjQbaf2t8_CE6JBrcWhpu_g9rdg9Pv2UmzZMqImu_MMQh21x8fe9H6eZz7oBV-Ta_7-MtH7PucGus_T3eL7y-5tnUOXnFnYCIe6xpd71e9E3CpEQLx2Cs7LoUiaQmrC7UiYbTzGAQV96vCCqcVbD5Dyge7/s692/no_markReactNative-snapshot-image_16.png" width="320" height="320"></a></center>

Berikut adalah langkah-langkah untuk membuat dan mengatur tugas terjadwal di OpenWrt:

## Langkah 1: Menginstal Paket Cron

Pertama, pastikan paket cron telah diinstal di perangkat OpenWrt Anda. Anda dapat melakukannya dengan menjalankan perintah berikut di terminal:

```bash
opkg update
opkg install cron
```

<center><a href="https://shope.ee/3L37VGNJOy" target="_blank"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg-mheNqpfyPhttt6bxh3dNYou58CsY5nHn1BnoU1R9-1I7nby81mIYFkW2Ye5eoUbPTAj1EXV12LuAUlGj8IELIv2Lo3vg5L7YUpxtowSUVu0HTV9y-mD3bIfFlmDsB-fx7I7Z1yFHN9V5JLpde8Ztbd2ynKhbj2F1VvtaRJlo8F1rhUZiP8YTHpr_FNgf/s692/no_markReactNative-snapshot-image_14.png" width="320" height="320"></a></center>

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

<center><a href="https://shope.ee/AUWHzCfxKa" target="_blank"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgpbULz3IUJfJ5bmJFaSCX7xGRZ-ghSiiN9rIUK8GtFT8hA09YYtqaHSFonXJEVO8yMu4tKPdnjozs2thxUOF96uBCJsrqG9-Nc23EkrztW0inoAgkyI52ZADPWR79FT4WPcMap91PiCFVgsGuKk7xBrfxBWvrC9jV_7GGtIhD_Zy5krYpyHI7iKNGClGZL/s320/no_markReactNative-snapshot-image_13.png" width="320" height="320"></a></center>

## Langkah 3: Memuat Ulang Cron

Setelah menyimpan perubahan pada file cron, pastikan untuk memuat ulang daemon cron agar perubahan tersebut berlaku:

```bash
/etc/init.d/cron reload
```

## Catatan Penting:

- Pastikan untuk memberikan perintah yang lengkap dan benar. Contoh, jika Anda ingin menjalankan skrip bash, pastikan untuk menyertakan jalur lengkap ke skrip tersebut (misalnya `/usr/bin/myscript.sh`).
- Selalu uji coba tugas terjadwal Anda dengan menambahkan tugas sederhana terlebih dahulu dan memeriksa apakah mereka dijalankan sesuai jadwal yang ditentukan.

<center><a href="https://shope.ee/8pO43diEs4" target="_blank"><img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhctCeCAHlKBLXbKXscZ3w2oZLwK9-foI3fqdYVTzk1p1jTBZunhmIC1FB_neNBtDmcJISzsPaP1S80c48RiYFirxdK7aRNSS7MHn_4jb5B8TpWc5lGJDnZ2jNNI-gEnzPfZHSZkK45mPzIX9frArr57txP8NE27FPkteG_4QrENkMecrlxfUjBhZcomRVp/s692/no_markReactNative-snapshot-image_15.png" width="320" height="320"></a></center>

Dengan mengikuti langkah-langkah di atas, Anda dapat dengan mudah mengatur dan menjalankan tugas terjadwal di perangkat OpenWrt Anda sesuai kebutuhan.

## Simak tutorial openwrt lainnya
{: .t60 }
{% include list-posts tag='openwrt' %}