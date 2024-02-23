---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: header_unsplash_12.jpg
widget1:
  title: "Tutorial Clash"
  url: 'https://yusuftutorial.xyz/clash/'
  text: 'Kita mulai dari <em>Konfigurasi</em> kemudian menuju ke <em>Proxies</em> lalu setelah itu <em>Proxy Provider</em> dan berlanjut ke <em>Proxy Groups</em>. Kemudian kita lanjutkan bagian <em>Rule Provider</em> kemudian <em>Mode Script</em> dan yang bagian akhir di <em>Ruleset</em>.'
  video: '<a href="#" data-reveal-id="videoclash"><img src="https://i.ytimg.com/an_webp/B22t3OgTvLQ/mqdefault_6s.webp" width="302" height="182" alt=""/></a>'
widget2:
  title: "Tutorial Openwrt"
  url: 'https://yusuftutorial.xyz/openwrt/'
  text: 'Kita akan memulai pembelajaran banyak hal tentang <em>openwrt</em>. Dan tentunya sangat simpel, sehingga sangat memudahkan anda untuk bisa lebih cepat mengatasi segala macam hal problem solving yang ada pada perangkat openwrt anda.'
  video: '<a href="#" data-reveal-id="videoopenwrt"><img src="https://i.ytimg.com/vi/5ypncHC-LUo/hqdefault.jpg" width="302" height="182" alt=""/></a>'
widget3:
  title: "Tutorial Mikrotik"
  url: 'https://yusuftutorial/mikrotik'
  text: 'Kita juga akan mempelajari bagaimana cara setup dasar pada mikrotik hingga bisa di gunakan dan tentunya anda akan lebih mudah untuk mandiri sendiri cara untuk settingnya.'
  video: '<a href="#" data-reveal-id="videomikrotik"><img src="https://i.ytimg.com/an_webp/2T6r3SQBL1I/mqdefault_6s.webp" width="302" height="182" alt=""/></a>'
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: https://youtube.com/@yusuftutorialchannel
  text: Simak semua video tutorial saya di channel youtube ›
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<div id="videoclash" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/B22t3OgTvLQ" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
<div id="videoopenwrt" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/5ypncHC-LUo" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
<div id="videomikrotik" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/5ypncHC-LUo" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>