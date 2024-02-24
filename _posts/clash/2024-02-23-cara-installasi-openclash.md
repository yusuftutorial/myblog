---
layout: page
sidebar: left
subheadline: Clash
title:  "Cara installasi Clash"
teaser: "Memasang dan setting dasar pada openclash di openwrt."
breadcrumb: true
tags:
    - openclash
categories:
    - basic
image:
    thumb: gallery-example-3-thumb.jpg
    title: gallery-example-3.jpg
    caption_url: https://yusuftutorial.xyz/clash/cara-installasi-clash/
---
Sebelum anda memulai langkah untuk menginstall openclash, alangkah baiknya anda untuk melengkapi semua keperluan dari openclash itu sendiri.

Mari kita masuk ke openwrt dan menuju ke terminal emulator.

## IP Tables
~~~
opkg update && opkg install coreutils-nohup bash iptables dnsmasq-full curl ca-certificates ipset ip-full iptables-mod-tproxy iptables-mod-extra libcap libcap-bin ruby ruby-yaml kmod-tun kmod-inet-diag unzip luci-compat luci luci-base
~~~

## NF Tables
~~~
opkg update && opkg install coreutils-nohup bash dnsmasq-full curl ca-certificates ipset ip-full libcap libcap-bin ruby ruby-yaml kmod-tun kmod-inet-diag unzip kmod-nft-tproxy luci-compat luci luci-base
~~~

Jika sudah semua selesai atau beres tanpa ada kendala. Mari kita lanjutkan ke tahap berikutnya.

Silahkan download file ipk clash [Disinj](https://github.com/vernesong/OpenClash/releases/download/v0.46.001-beta/luci-app-openclash_0.46.001-beta_all.ipk)

Kemudian taruh ke folder root pada file manager openwrt.

Setelah itu kembali masuk ke terminal emulator dan ketikkan berikut ini.

~~~
cd /root
opkg install *.ipk
~~~

Tunggu hingga selesai, setelah beres anda tinggal reboot perangkat.


## Simak post tentang clash lainnya
{: .t60 }
{% include list-posts tag='openclash' %}