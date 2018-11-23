![Image of IDElabs](/images/IDElabs-logo.png)

# movinsing-android

## DEVELOPER GUIDE

Please read the documentation carefully, and if you have any questions please check to me.
> SAFE HARBOUR

> *sourcecode ini hanya boleh untuk anggota IDElabs team yang masih aktif, dan hanya untuk keperluan perusahaan2 yang berafiliasi dengan IDElabs (mis: IDE2SEN, DEFGHI). Diluar dari yang disebutkan diatas jelas-jelas merupakan tindakan melawan hukum.*

Untuk mulai coding, kalian perlu menginstal *Android Studio*.  juga membutuhkan *Java SE Development Kit*.

Pertama, download Android Studio di (https://developer.android.com/studio/index.html). Selanjutnya, kalian akan diarahkan ke petunjuk pemasangan (https://developer.android.com/studio/install.html) yang menyediakan petunjuk tentang instalasi Android Studio,  download untuk JDK di (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

### SDK Manager
Installer, seperti juga ditunjukkan dalam video, harus secara otomatis download semua komponen yang diperlukan.
Jika melakukan manual setting, download minimal komponen berikut lewat SDK manager:
1. SDK Tools
2. SDK Platform Tools
3. SDK Build Tools
4. Google Play Services 
5. Android Support Library 
6. Android Support Repository 
7. Google Repository
8. Google USB Driver

Untuk bisa menggunakan movinsing-android-code ini, kalian memerlukan versi SDK default dari movinsing-android-code  ini pada saat ditulis yaitu, *Marshmallow*.

Kalian download SDK ini, jika belum diinstal, lewat SDK Manager[SDK(https://developer.android.com/studio/intro/update.html#sdk-manager)

### Wordpress Preparation

Mempersiapkan Blog Wordpress kalian untuk dijadikan content feed untuk aplikasi ini, kalian perlu menginstal plugin JSON API atau menggunakan  REST API Wordpress. 

#### REST API
REST API secara default disediakan untuk blog Wordpress.com, dan untuk blog Wordpress yang dihosting sendiri yang menginstall plugin JetPack [JrtPack]((https://wordpress.org/plugins/jetpack/). Pastikan bahwa situs yg kalian buat tsb dapat diakses melalui REST API dengan mengunjungi https://public-api.wordpress.com/rest/v1/sites/YOURBLOG

Di mana YOURBLOG dapat menjadi ID Blog kalian (misalnya 3584907) atau domain blog kalian tanpa http (mis. Www.artifacting.com (http://www.artifacting.com) atau en.blog.wordpress.com).

#### JSON API
Jika kalian memiliki blog yang dihosting sendiri dan tidak ingin menggunakan Jetpack, kalian dapat menggunakan plugin JSON-API.
1. Pertama-tama kalian harus mengunduh plugin, lebih disukai versi stable yaitu 1.1.1
di http://wordpress.org/plugins/json-api/developers/ [JSONAPI](http://wordpress.org/plugins/json-api/developers/).
2. Download folder `json-api` ke direktori` / wp-content / plugins / `atau instal langsung melalui  plugin installer.
3. Aktifkan plugin melalui menu 'Plugins' di WordPress atau dengan menggunakan link yang disediakan oleh  plugin installer.
4. Aktifkan user-friendly URL dari Settings > Permalinks, gunakan format the "Day and name".
5. Pastikan url API kalian dan gunakan untuk item Wordpress, biasanya akan menjadi seperti:
"yourblogurl.com/api/".

## Mulai Coding di Android Studio
### Importing
Untuk mengimpor movinsing-android-code, cukup cloning github ini, dan buka di Android Studio dengan pilih ‘Open Existing Project’. Pastikan untuk menunggu semua proses (Gradle Build) selesai sebelum melanjutkan ke langkah berikutnya.

### Addition steps
Terkadang, Build Gradle gagal. Dalam beberapa kasus, komponen tambahan diperlukan, Android Studio biasanya meminta untuk download SDK components tambahan ini di tab ‘messages’, cukup ikuti petunjuk yang diberikan untuk menginstal dan download segera komponen-komponen tambahan tersebut.

## Content
Menu / konten aplikasi tempate ditentukan dalam file konfigurasi. Bersama movinsing-android-code ini saya bangun tools untuk membuat file konfigurasi yang dapat dikunjungi menggunakan link ini https://webservice.id/help/movinsing-android-code-configurator/. Setelah selesai membuat konfigurasi, unduh file konfigurasi (config.json) itu untuk digunakan di langkah berikutnya.

Dengan file config.json itu kalian dengan mudhny dapat mengkonfigurasi aplikasi movinsing-android-code kapan saja, namun tentu saja dengan gunakan beberapa informasi dasar yang telah disepakati oleh semua anggoa tim, seperti kunci API, nama aplikasi dlsb. 


## USER GUIDE

# tempate for Android Devices
###### --  Sat 10 Nov 2018 by tomsX from IDElabs please treat this gits as private and strictly confidential.

## Introduction
DEFGHI's Develepmont & Deployment Team, IDElabs telah membangun membuat aplikasi  tempate ini yang menggunakan integrasi dengan berbagai penyedia konten. Tata letak menu sepenuhnya dapat disesuaikan (ikon, judul, bagian), selain itu kalian dapat menambahkan banyak item ke menu yang kalian inginkan. 

## Alat Pengaturan Content
Pengaturan saat ini hanya untuk klarifikasi bagian item dari content, kami sudah buatkan tools khusus, yang kita sebut 'Configurator', berupa GUI untuk pengguna dapat mengatur content didalam aplikasi ini, dan kemudian menyiman pengaturan tersebut ke satu file config.json.
Lalu file config.json ini disimpan ke dalam direktori /app/src/main/asset didalam project folder. (bila sudah ada file tersebut, maka jangan lupa untuk menduplikasikannya dahulu sebelum melakukan 'replace').
Cara menggunakan configurator menentukan isi dari aplikasi, dan itu semua tanpa menulis satu baris kode. Gunakan drawer, atas & bawah tab, dan kategori layar untuk menavigasi konten.

## Design
Dibuat untuk design layar besar dan kecil yang paling intuitif. Berdasarkan Material Design yang akan terlihat menakjubkan pada semua perangkat Android.
Dirancang untuk konten tempate, Kami telah menciptakan layout khusus untuk semua konten tempate kami. Dengan cara ini, kami dapat memberikan konten yang layak menjadi perhatian .
 
## Fitur yang sudah bisa di gunakan
Menakjubkan fitur built-in untuk memberikan kalian start yang mudah. Termasuk fitur yang mudah untuk di monetisasi.
#### In-App Purchases 
• Unlock extra content and remove ads
#### Push Notifications
• Send messages and urls to users
#### Admob Advertising
• Show banner & interstitial ads
#### MediaPlayer 
• Built-in viewer for all your media
#### Remote Config
• Change your app's content on the fly
#### Integration
• Easily add custom fragments/activities
#### Localisation
• Easy translation & RTL support
#### Tablet Support 
• Dedicated layouts for large screens

## Integrasi Provider ke Item
tempate mendukung integrasi ke banyak penyedia konten untuk memastikan dapat menampilkan konten dari seluruh web. Pertama, tempate mendukung Wordpress untuk menampilkan posting blog Wordpress, baik dari Wordpress.com atau situs Wordpress yang di-hosting sendiri. Selanjutnya, tempate mendukung Youtube untuk menunjukkan saluran Youtube, daftar putar Youtube atau live video. Radio juga didukung sehingga pengguna dapat mendengarkan streaming Radio atau Shoutcast / Icecast di aplikasi tempate (dengan metadata / informasi Now Playing). WooCommerce untuk mengintegrasikan Toko WooCommerce ke dalam aplikasi tempate, pengguna dapat menelusuri produk, menambahkannya ke keranjang, checkout, masuk dan melihat pesanan terbaru mereka. WebView tersedia untuk menampilkan halaman web, baik online maupun offline. Facebook untuk menunjukkan feed halaman Facebook. TV & Live Streaming untuk menampilkan Live TV dan Streaming video dalam HD. SoundCloud untuk memutar playlist SoundCloud dan user's upload. RSS dan Podcast untuk menampilkan feed RSS dan artikel di aplikasi tempate. Instagram, untuk menampilkan posting Instagram. Tumblr, untuk menampilkan galeri gambar Tumblr. Flickr, untuk menampilkan galeri atau album Flickr. Twitter untuk menampilkan tweet berdasarkan hashtag, query, atau username. Maps, untuk menampilkan lokasi GeoJSON di aplikasi tempate. Dan pinterest untuk menampilkan Pinterest Board.

Dibawah ini adalah daftar provider yang sudah bisa digunakan dengan deskripsi yang lebih detail dari masing-masing penyedia konten:

#### WebView
• Mengubah website kalian menjadi aplikasi. Termasuk situs web, aplikasi web atau halaman web di aplikasi kalian. 
+ Dukungan untuk HTML5. Video, Download, Intents & Lainnya
+ Pull to Refresh, untuk menyegarkan dan (opsional) Back & Forward navigation
+ Menyajikan halaman web secara offline sebaik online 

#### WordPress
• Menampilkan Blog Wordpress tempate ke dalam Aplikasi tempate Android
+ Home screen dengan highluighted post dan category slider 
+ Paralaks tata letak post, dengan featured image & related posts
+ integrasi ke Disqus dan native WP comments 
+ Layajan Built-in untuk lampiran dan gallery

#### YouTube
• Tambahkan semua channel, playlist dan streaming langsung ke aplikasi
+ Home screen dengan highlighted video & pencarian
+ Built-in Pemutar Youtube yang mendukung 4K, 360", Live & 60FPS 
+ Mendukung live stream, playlist dan channel
+ Paralaks halaman video dengan keterangan & komentar

## Features
#### Unlimited Items –
kalian dapat menggunakan & menggabungkan sebanyak Timelines, Blog, Feed, Channels, Playlists, Stations, Webpages, dll seperti yang kalian inginkan. Opsional tambahkan ikon, buat sections dan highlights.
#### Material Design – 
Material Design Lengkap, dengan Drawer Icon, Ripple’s dan tata letak Card. Sepenuhnya dapat disesuaikan dalam setiap warna. Dengan animasi halus seperti header paralaks dan toolbar memudar.
#### Tablet UI – 
Tata letak dua plane yang diarahka penggunaanya pada tablet dan detailview yang imersif untuk memudahkan membaca artikel dan melihat konten tanpa ada rasa terganggu.
#### Push Notifications by OneSignal – 
Kirim pesan push dan url ke pengguna kalian dengan mudah
#### In-App purchase – 
Biarkan pengguna kalian menghapus iklan atau membuka ekstra kunci konten dengan melakukan pembelian di dalam aplikasi *
#### Offline & Favorites – 
Menyimpan Artikel dan posting dari Wordpress dan RSS offline. Halaman web & video Youtube dapat dikirimkan sebagai favorit. Gambar Tumblr dapat disimpan ke penyimpanan lokal.
#### Customizable – 
Buat aplikasi kalian dengan mudah melalui alat penerjemah, dan dengan menyesuaikan warna & menggunakan ikon kalian sendiri untuk menu. kalian juga dapat memilih antara beberapa gaya untuk panel samping Navigasi , misalnya dengan mengatur gambar header

###### --  Sat 10 Nov 2018 by tomsX from IDElabs please treat this gits as private and strictly confidential.
