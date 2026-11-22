# Nocturne Rail - Latihan Git dan GitHub

Repository ini adalah website statis kecil untuk **Nocturne**, sebuah perusahaan kereta tidur fiktif. Repository ini dipakai untuk berlatih branch, commit, push, dan pull request.

Halaman utama (`index.html`) dan stylesheet-nya (`styles.css`) sudah disiapkan. Navigasi di halaman utama menuju tujuh halaman yang belum ada. Setiap siswa membuat tepat satu halaman.

## Isi repository

| File | Status |
|---|---|
| `index.html` | Halaman utama, sudah dibuat. Jangan diubah. |
| `styles.css` | Sistem desain bersama, sudah dibuat. Jangan diubah. |
| `README.md` | File ini. Berisi prompt tugas Anda. |

## Alur kerja kelas

1. Clone repository ini ke komputer Anda.
2. Buat branch dengan nama `add/<halaman>-<namauser>`, misalnya `add/routes-siti`.
3. Cari halaman Anda di tabel pembagian tugas di bawah. Salin **hanya prompt Anda** dari README ini, lalu tempel ke agen AI.
4. Lihat pratinjau halaman dengan membuka file HTML baru tersebut di browser.
5. Lakukan stage dan commit untuk file baru Anda, lalu push branch Anda.
6. Buat pull request ke `main`. PR Anda seharusnya hanya menambah file.

Karena tidak ada yang mengubah `index.html` atau `styles.css`, pull request satu dengan lainnya tidak akan bertabrakan.

## Pembagian tugas

| # | Halaman yang dibuat | File baru | Contoh branch |
|---|---|---|---|
| 1 | Rute dan jadwal | `routes.html`, opsional `routes.css` | `add/routes-devan` |
| 2 | Kabin dan tempat tidur | `cabins.html`, opsional `cabins.css` | `add/cabins-dhani` |
| 3 | Makanan di kereta | `dining.html`, opsional `dining.css` | `add/dining-ifadha` |
| 4 | Jurnal perjalanan | `journal.html`, opsional `journal.css` | `add/journal-karin` |
| 5 | Galeri | `gallery.html`, opsional `gallery.css` | `add/gallery-nisa` |
| 6 | Tentang kami | `about.html`, opsional `about.css` | `add/about-sapna` |
| 7 | Kontak dan pemesanan | `contact.html`, opsional `contact.css` | `add/contact-serli` |

Satu halaman untuk satu siswa. Tulis nama Anda di sebelah baris tugas Anda saat di kelas agar tidak ada yang mengambil halaman yang sama.

## Prompt

Setiap prompt di bawah sudah lengkap dengan sendirinya. Salin seluruh blok, termasuk bagian CONTEXT dan ATURAN KUALITAS, lalu tempel ke agen Anda.

### 1. Rute dan jadwal (Devan)

```text
CONTEXT
Anda berkontribusi pada website statis kecil di folder ini: situs demo untuk "Nocturne", sebuah perusahaan kereta tidur fiktif. File index.html dan styles.css sudah disiapkan sebelumnya. Baca KEDUA file terlebih dahulu dan samakan persis.

Sistem desain yang harus dipakai ulang:
- Font dimuat di <head> dari Google Fonts: Syne untuk judul, DM Sans untuk teks isi, IBM Plex Mono untuk label, jam, dan data.
- Variabel CSS di styles.css: --ink #171b3d, --ink-deep #0d1030, --page #f6f8fc, --panel #e8edf6, --paper #ffffff, --slate #4d5375, --line #ccd3e2, --brass #f0a93b. Pakai variabel tersebut, jangan menciptakan warna baru.
- Kelas yang sudah ada dan harus dipakai ulang: .eyebrow, .section-lede, .btn, .btn-solid, .btn-brass, .text-link, .board, .ticket, .ticket-rack, .site-header, .site-footer, .strip-inner.
- Salin <head>, header, dan footer dari index.html ke halaman baru Anda agar semua halaman tampak seperti satu website yang sama. Pertahankan ketujuh tautan navigasi. Di halaman Anda saja, hapus label "soon" dari setiap tautan ke halaman Routes (header, menu mobile, dan footer). Jangan edit index.html.
- Teks antarmuka tetap dalam bahasa Inggris agar konsisten dengan halaman utama. Contoh kalimat di bawah sudah dalam bahasa Inggris.

ATURAN FILE YANG KETAT
- Buat HANYA routes.html dan, jika perlu gaya khusus halaman, routes.css. Hubungkan routes.css setelah styles.css di <head>.
- JANGAN ubah index.html atau styles.css. Ini membuat setiap pull request bebas konflik.
- Tanpa framework, tanpa UI kit CDN, tanpa atribut style inline. CSS eksternal saja.

ATURAN KUALITAS
- Responsif hingga 360px: tidak ada overflow horizontal, tidak ada teks terpotong, target sentuh minimal 44px.
- Pertahankan gaya fokus keyboard yang sudah didefinisikan secara global dan hormati prefers-reduced-motion.
- Jangan gunakan em dash. Jangan mengarang statistik, testimoni pelanggan, nama anggota tim, atau foto stok.
- Gunakan teks yang konkret dan sederhana dengan suara perusahaan kereta, bukan jargon pemasaran.
- Hindari label CTA umum seperti Get Started, Learn More, Explore, atau Discover.

TUGAS ANDA
Buat routes.html, halaman jadwal. Isinya:

1. Bagian pembuka dengan label kecil "The network", judul besar Syne seperti "Every line, one timetable.", dan paragraf pembuka singkat yang menjelaskan bahwa semua layanan berangkat sore hari dan tiba sebelum jam sibuk pagi.
2. Tabel HTML semantik berjudul "Tonight's departures" dengan kolom: Service, Route, Depart, Arrive, Days, Fare. Pakai warna board dan huruf mono yang sudah ada untuk data. Isi enam baris. Samakan dengan halaman utama: N 102 London ke Paris 21:40 / 08:15, N 214 Paris ke Vienna 22:10 / 09:35, N 308 Prague ke Milan 20:55 / 07:40, dan N 416 London ke Copenhagen 23:05 / 10:20. Tambahkan dua layanan lain dengan kode dan jam bergaya sama. Tandai satu baris dengan status "Boarding" berwarna kuning brass.
3. Tiga blok detail rute memakai kelas .ticket-rack dan .ticket: London ke Paris, Paris ke Vienna, Prague ke Milan. Tiap blok berisi kode rute, tag singkat, jam berangkat dan tiba, tarif yang konsisten dengan halaman utama, serta dua kalimat tentang pemandangan dari jendela.
4. Catatan singkat "Reading the board" yang menjelaskan bahwa waktu yang dipakai adalah waktu setempat, check-in dibuka sembilan puluh menit sebelum keberangkatan, dan status boarding menyala menjelang keberangkatan.
5. Bagian CTA penutup yang menuju ke cabins.html dengan label "Choose your berth".

Gunakan <table> dengan <thead>, <tbody>, <th scope="col"> dan <caption> agar jadwal bisa dibaca pembaca layar. Pada layar sempit, buat tabel bergulir horizontal di dalam wadahnya sendiri, bukan meluap keluar halaman.

Jangan menjalankan perintah git apa pun. Setelah selesai, sebutkan file yang Anda buat dan cara melihat pratinjau halaman secara lokal.
```

### 2. Kabin dan tempat tidur (Dhani)

```text
CONTEXT
Anda berkontribusi pada website statis kecil di folder ini: situs demo untuk "Nocturne", sebuah perusahaan kereta tidur fiktif. File index.html dan styles.css sudah disiapkan sebelumnya. Baca KEDUA file terlebih dahulu dan samakan persis.

Sistem desain yang harus dipakai ulang:
- Font dimuat di <head> dari Google Fonts: Syne untuk judul, DM Sans untuk teks isi, IBM Plex Mono untuk label, jam, dan data.
- Variabel CSS di styles.css: --ink #171b3d, --ink-deep #0d1030, --page #f6f8fc, --panel #e8edf6, --paper #ffffff, --slate #4d5375, --line #ccd3e2, --brass #f0a93b. Pakai variabel tersebut, jangan menciptakan warna baru.
- Kelas yang sudah ada dan harus dipakai ulang: .eyebrow, .section-lede, .btn, .btn-solid, .btn-brass, .text-link, .berth-specs, .window-frame, .window-sky, .window-sill, .site-header, .site-footer, .strip-inner.
- Salin <head>, header, dan footer dari index.html ke halaman baru Anda agar semua halaman tampak seperti satu website yang sama. Pertahankan ketujuh tautan navigasi. Di halaman Anda saja, hapus label "soon" dari setiap tautan ke halaman Cabins (header, menu mobile, dan footer). Jangan edit index.html.
- Teks antarmuka tetap dalam bahasa Inggris agar konsisten dengan halaman utama. Contoh kalimat di bawah sudah dalam bahasa Inggris.

ATURAN FILE YANG KETAT
- Buat HANYA cabins.html dan, jika perlu gaya khusus halaman, cabins.css. Hubungkan cabins.css setelah styles.css di <head>.
- JANGAN ubah index.html atau styles.css. Ini membuat setiap pull request bebas konflik.
- Tanpa framework, tanpa UI kit CDN, tanpa atribut style inline. CSS eksternal saja.

ATURAN KUALITAS
- Responsif hingga 360px: tidak ada overflow horizontal, tidak ada teks terpotong, target sentuh minimal 44px.
- Pertahankan gaya fokus keyboard yang sudah didefinisikan secara global dan hormati prefers-reduced-motion.
- Jangan gunakan em dash. Jangan mengarang statistik, testimoni pelanggan, nama anggota tim, atau foto stok.
- Gunakan teks yang konkret dan sederhana dengan suara perusahaan kereta, bukan jargon pemasaran.
- Hindari label CTA umum seperti Get Started, Learn More, Explore, atau Discover.

TUGAS ANDA
Buat cabins.html, halaman yang menjelaskan tempat tidur penumpang. Isinya:

1. Bagian pembuka dengan label kecil "On board", judul besar Syne seperti "A room that moves.", dan paragraf pembuka tentang tertidur di satu kota lalu bangun di kota lain.
2. Visual memakai adegan jendela CSS-only dari index.html: salin markup .window-frame dengan bintang, bulan, dan ambang jendela. Tambahkan keterangan yang jujur seperti "View from an upper berth, illustrated". Jangan pakai foto.
3. Tiga pilihan kabin yang ditampilkan secara berbeda, bukan tiga kartu yang identik: kursi sandar untuk perjalanan pendek, kompartemen dua tempat tidur untuk sebagian besar perjalanan, dan kabin single pribadi bagi yang ingin sendirian. Untuk tiap pilihan sebutkan siapa yang cocok, jenis tempat tidur, meja, ruang bagasi, dan biaya tambahan dalam euro. Jadikan kompartemen dua tempat tidur sebagai yang paling menonjol.
4. Tabel perbandingan memakai HTML semantik untuk spesifikasi ketiga pilihan. Pakai <th scope="row"> untuk label baris dan sebuah <caption>.
5. Daftar "Included in every berth" berisi sprei, kopi bangun tidur, lampu baca, colokan listrik, dan pintu yang bisa dikunci.
6. Catatan singkat "Before you board" dengan tiga tips praktis, misalnya membawa sandal dan menyiapkan tiket.
7. CTA penutup ke dining.html dengan label "See what is served on board".

Jangan menjalankan perintah git apa pun. Setelah selesai, sebutkan file yang Anda buat dan cara melihat pratinjau halaman secara lokal.
```

### 3. Makanan di kereta (Ifa)

```text
CONTEXT
Anda berkontribusi pada website statis kecil di folder ini: situs demo untuk "Nocturne", sebuah perusahaan kereta tidur fiktif. File index.html dan styles.css sudah disiapkan sebelumnya. Baca KEDUA file terlebih dahulu dan samakan persis.

Sistem desain yang harus dipakai ulang:
- Font dimuat di <head> dari Google Fonts: Syne untuk judul, DM Sans untuk teks isi, IBM Plex Mono untuk label, jam, dan data.
- Variabel CSS di styles.css: --ink #171b3d, --ink-deep #0d1030, --page #f6f8fc, --panel #e8edf6, --paper #ffffff, --slate #4d5375, --line #ccd3e2, --brass #f0a93b. Pakai variabel tersebut, jangan menciptakan warna baru.
- Kelas yang sudah ada dan harus dipakai ulang: .eyebrow, .section-lede, .btn, .btn-solid, .btn-brass, .text-link, .eyebrow-rule, .site-header, .site-footer, .strip-inner.
- Salin <head>, header, dan footer dari index.html ke halaman baru Anda agar semua halaman tampak seperti satu website yang sama. Pertahankan ketujuh tautan navigasi. Di halaman Anda saja, hapus label "soon" dari setiap tautan ke halaman Dining (header, menu mobile, dan footer). Jangan edit index.html.
- Teks antarmuka tetap dalam bahasa Inggris agar konsisten dengan halaman utama. Contoh kalimat di bawah sudah dalam bahasa Inggris.

ATURAN FILE YANG KETAT
- Buat HANYA dining.html dan, jika perlu gaya khusus halaman, dining.css. Hubungkan dining.css setelah styles.css di <head>.
- JANGAN ubah index.html atau styles.css. Ini membuat setiap pull request bebas konflik.
- Tanpa framework, tanpa UI kit CDN, tanpa atribut style inline. CSS eksternal saja.

ATURAN KUALITAS
- Responsif hingga 360px: tidak ada overflow horizontal, tidak ada teks terpotong, target sentuh minimal 44px.
- Pertahankan gaya fokus keyboard yang sudah didefinisikan secara global dan hormati prefers-reduced-motion.
- Jangan gunakan em dash. Jangan mengarang statistik, testimoni pelanggan, nama anggota tim, atau foto stok.
- Gunakan teks yang konkret dan sederhana dengan suara perusahaan kereta, bukan jargon pemasaran.
- Hindari label CTA umum seperti Get Started, Learn More, Explore, atau Discover.

TUGAS ANDA
Buat dining.html, halaman tentang makanan di atas kereta. Isinya:

1. Bagian pembuka dengan label kecil "On board", judul besar Syne seperti "Dinner, then a bed.", dan paragraf pembuka tentang makan di gerbong makan saat pemandangan lewat.
2. Contoh menu malam dalam tiga bagian. Tiap bagian berisi dua atau tiga pilihan dengan deskripsi singkat dan harga dalam euro. Pakai garis titik-titik antara nama masakan dan harga, atau kolom harga mono, bukan kartu umum. Pilih makanan yang masuk akal untuk kereta tidur Eropa.
3. Blok "Morning service" yang menjelaskan sarapan disajikan sebelum tiba, dengan kopi dan roti, dan sudah termasuk dengan tempat tidur.
4. Daftar jam layanan dengan empat entri: minuman menyambut setelah naik kereta, dua sesi makan malam, dan sarapan. Tampilkan jam dengan huruf mono, dan sebutkan gerbong makan tutup sebelum kereta tiba di tujuan.
5. Catatan singkat tentang pilihan vegetarian, vegan, dan bebas gluten, serta meminta penumpang menyampaikannya saat memesan.
6. CTA penutup ke routes.html dengan label "Pick a line".

Jangan mengarang nama koki, penghargaan, atau rating. Jangan menjalankan perintah git apa pun. Setelah selesai, sebutkan file yang Anda buat dan cara melihat pratinjau halaman secara lokal.
```

### 4. Jurnal perjalanan (Karin)

```text
CONTEXT
Anda berkontribusi pada website statis kecil di folder ini: situs demo untuk "Nocturne", sebuah perusahaan kereta tidur fiktif. File index.html dan styles.css sudah disiapkan sebelumnya. Baca KEDUA file terlebih dahulu dan samakan persis.

Sistem desain yang harus dipakai ulang:
- Font dimuat di <head> dari Google Fonts: Syne untuk judul, DM Sans untuk teks isi, IBM Plex Mono untuk label, jam, dan data.
- Variabel CSS di styles.css: --ink #171b3d, --ink-deep #0d1030, --page #f6f8fc, --panel #e8edf6, --paper #ffffff, --slate #4d5375, --line #ccd3e2, --brass #f0a93b. Pakai variabel tersebut, jangan menciptakan warna baru.
- Kelas yang sudah ada dan harus dipakai ulang: .eyebrow, .section-lede, .btn, .btn-solid, .btn-brass, .text-link, .journal-quote, .journal-issue, .site-header, .site-footer, .strip-inner.
- Salin <head>, header, dan footer dari index.html ke halaman baru Anda agar semua halaman tampak seperti satu website yang sama. Pertahankan ketujuh tautan navigasi. Di halaman Anda saja, hapus label "soon" dari setiap tautan ke halaman Journal (header, menu mobile, dan footer). Jangan edit index.html.
- Teks antarmuka tetap dalam bahasa Inggris agar konsisten dengan halaman utama. Contoh kalimat di bawah sudah dalam bahasa Inggris.

ATURAN FILE YANG KETAT
- Buat HANYA journal.html dan, jika perlu gaya khusus halaman, journal.css. Hubungkan journal.css setelah styles.css di <head>.
- JANGAN ubah index.html atau styles.css. Ini membuat setiap pull request bebas konflik.
- Tanpa framework, tanpa UI kit CDN, tanpa atribut style inline. CSS eksternal saja.

ATURAN KUALITAS
- Responsif hingga 360px: tidak ada overflow horizontal, tidak ada teks terpotong, target sentuh minimal 44px.
- Pertahankan gaya fokus keyboard yang sudah didefinisikan secara global dan hormati prefers-reduced-motion.
- Jangan gunakan em dash. Jangan mengarang statistik, testimoni pelanggan, nama anggota tim, atau foto stok.
- Gunakan teks yang konkret dan sederhana dengan suara perusahaan kereta, bukan jargon pemasaran.
- Hindari label CTA umum seperti Get Started, Learn More, Explore, atau Discover.

TUGAS ANDA
Buat journal.html, indeks editorial berisi artikel singkat. Isinya:

1. Bagian pembuka dengan label kecil "From the journal", judul besar Syne seperti "Notes from the night train.", dan paragraf pembuka tentang catatan dari orang-orang yang menjalankan dan menggunakan kereta.
2. Blok artikel utama. Pakai ulang kutipan dari halaman utama, "The best part of the trip was the part I slept through.", dengan atribusi "Notes from the Paris line". Tambahkan label edisi, kategori, dan lama baca. Beri blok ini huruf yang jauh lebih besar dari bagian lain di halaman.
3. Daftar "Recent dispatches" dengan empat artikel. Tiap entri berisi tanggal mono singkat, judul, ringkasan dua baris, tag kategori, dan lama baca. Jadikan judul sebagai fokus visual utama dan biarkan metadata tetap tenang. Angkat topik kereta tidur yang masuk akal: perjalanan pertama dengan kereta tidur, apa yang diperiksa kondektur sebelum berangkat, menyeberang perbatasan malam hari, dan suara stasiun saat fajar.
4. Sidebar kecil "About the journal" dengan dua atau tiga kalimat tentang apa yang diterbitkan di sini. Atribusikan tulisan ke "Nocturne editors" atau "Onboard notes". Jangan buat nama penulis atau foto profil.
5. CTA penutup ke about.html dengan label "Who we are".

Pakai elemen <article>, <time>, dan <blockquote> jika sesuai. Jangan menjalankan perintah git apa pun. Setelah selesai, sebutkan file yang Anda buat dan cara melihat pratinjau halaman secara lokal.
```

### 5. Galeri (Nisa)

```text
CONTEXT
Anda berkontribusi pada website statis kecil di folder ini: situs demo untuk "Nocturne", sebuah perusahaan kereta tidur fiktif. File index.html dan styles.css sudah disiapkan sebelumnya. Baca KEDUA file terlebih dahulu dan samakan persis.

Sistem desain yang harus dipakai ulang:
- Font dimuat di <head> dari Google Fonts: Syne untuk judul, DM Sans untuk teks isi, IBM Plex Mono untuk label, jam, dan data.
- Variabel CSS di styles.css: --ink #171b3d, --ink-deep #0d1030, --page #f6f8fc, --panel #e8edf6, --paper #ffffff, --slate #4d5375, --line #ccd3e2, --brass #f0a93b. Pakai variabel tersebut, jangan menciptakan warna baru.
- Kelas yang sudah ada dan harus dipakai ulang: .eyebrow, .section-lede, .btn, .btn-solid, .btn-brass, .text-link, .window-frame, .window-sky, .window-sill, .ticket, .site-header, .site-footer, .strip-inner.
- Salin <head>, header, dan footer dari index.html ke halaman baru Anda agar semua halaman tampak seperti satu website yang sama. Pertahankan ketujuh tautan navigasi. Di halaman Anda saja, hapus label "soon" dari setiap tautan ke halaman Gallery (header, menu mobile, dan footer). Jangan edit index.html.
- Teks antarmuka tetap dalam bahasa Inggris agar konsisten dengan halaman utama. Contoh kalimat di bawah sudah dalam bahasa Inggris.

ATURAN FILE YANG KETAT
- Buat HANYA gallery.html dan, jika perlu gaya khusus halaman, gallery.css. Hubungkan gallery.css setelah styles.css di <head>.
- JANGAN ubah index.html atau styles.css. Ini membuat setiap pull request bebas konflik.
- Tanpa framework, tanpa UI kit CDN, tanpa atribut style inline. CSS eksternal saja.

ATURAN KUALITAS
- Responsif hingga 360px: tidak ada overflow horizontal, tidak ada teks terpotong, target sentuh minimal 44px.
- Pertahankan gaya fokus keyboard yang sudah didefinisikan secara global dan hormati prefers-reduced-motion.
- Jangan gunakan em dash. Jangan mengarang statistik, testimoni pelanggan, nama anggota tim, atau foto stok.
- Gunakan teks yang konkret dan sederhana dengan suara perusahaan kereta, bukan jargon pemasaran.
- Hindari label CTA umum seperti Get Started, Learn More, Explore, atau Discover.

TUGAS ANDA
Buat gallery.html, halaman visual tanpa gambar eksternal. Semua yang ditampilkan harus berupa ilustrasi CSS orisinal yang dibangun dari bentuk sederhana, warna solid, dan box shadow. Jangan pakai gradien, URL gambar, atau layanan foto placeholder.

1. Bagian pembuka dengan label kecil "Gallery", judul besar Syne seperti "The view from the window.", dan paragraf pembuka.
2. Enam panel ilustrasi dalam bingkai dengan keterangan jujur yang menyebut isinya, misalnya "Illustration: a night window with a brass moon". Adegan yang disarankan: jendela malam dengan bintang dan bulan, terowongan yang terbuka ke fajar, peron stasiun kosong di bawah lampu, selimut terlipat di tempat tidur bawah, cangkir dan tiket terlipat di meja, serta deretan gerbong tidur dari luar. Bangun dengan div dan CSS, pakai ulang ide .window-frame jika membantu.
3. Tata letak yang bervariasi, bukan grid seragam: satu panel besar, empat panel lebih kecil di sekitarnya, dan satu panel lebar di bawah. Variasikan rasio ukuran. Biarkan halaman tetap tenang dan ilustrasi yang menjadi fokus.
4. Catatan jujur singkat di bawah grid yang menjelaskan bahwa ini ilustrasi gambar untuk situs demo, bukan foto layanan sungguhan.
5. CTA penutup ke journal.html dengan label "Read the dispatches".

Berikan keterangan teks yang bermakna pada setiap panel. Jangan menjalankan perintah git apa pun. Setelah selesai, sebutkan file yang Anda buat dan cara melihat pratinjau halaman secara lokal.
```

### 6. Tentang kami (Sapna)

```text
CONTEXT
Anda berkontribusi pada website statis kecil di folder ini: situs demo untuk "Nocturne", sebuah perusahaan kereta tidur fiktif. File index.html dan styles.css sudah disiapkan sebelumnya. Baca KEDUA file terlebih dahulu dan samakan persis.

Sistem desain yang harus dipakai ulang:
- Font dimuat di <head> dari Google Fonts: Syne untuk judul, DM Sans untuk teks isi, IBM Plex Mono untuk label, jam, dan data.
- Variabel CSS di styles.css: --ink #171b3d, --ink-deep #0d1030, --page #f6f8fc, --panel #e8edf6, --paper #ffffff, --slate #4d5375, --line #ccd3e2, --brass #f0a93b. Pakai variabel tersebut, jangan menciptakan warna baru.
- Kelas yang sudah ada dan harus dipakai ulang: .eyebrow, .section-lede, .btn, .btn-solid, .btn-brass, .text-link, .reason, .reason-label, .site-header, .site-footer, .strip-inner.
- Salin <head>, header, dan footer dari index.html ke halaman baru Anda agar semua halaman tampak seperti satu website yang sama. Pertahankan ketujuh tautan navigasi. Di halaman Anda saja, hapus label "soon" dari setiap tautan ke halaman About (header, menu mobile, dan footer). Jangan edit index.html.
- Teks antarmuka tetap dalam bahasa Inggris agar konsisten dengan halaman utama. Contoh kalimat di bawah sudah dalam bahasa Inggris.

ATURAN FILE YANG KETAT
- Buat HANYA about.html dan, jika perlu gaya khusus halaman, about.css. Hubungkan about.css setelah styles.css di <head>.
- JANGAN ubah index.html atau styles.css. Ini membuat setiap pull request bebas konflik.
- Tanpa framework, tanpa UI kit CDN, tanpa atribut style inline. CSS eksternal saja.

ATURAN KUALITAS
- Responsif hingga 360px: tidak ada overflow horizontal, tidak ada teks terpotong, target sentuh minimal 44px.
- Pertahankan gaya fokus keyboard yang sudah didefinisikan secara global dan hormati prefers-reduced-motion.
- Jangan gunakan em dash. Jangan mengarang statistik, testimoni pelanggan, nama anggota tim, atau foto stok.
- Gunakan teks yang konkret dan sederhana dengan suara perusahaan kereta, bukan jargon pemasaran.
- Hindari label CTA umum seperti Get Started, Learn More, Explore, atau Discover.

TUGAS ANDA
Buat about.html, halaman yang menjelaskan alasan perusahaan ini ada. Isinya:

1. Bagian pembuka dengan label kecil "About Nocturne", judul besar Syne seperti "We run trains so you can sleep.", dan pernyataan misi dua kalimat.
2. Bagian "How we work" dengan tiga prinsip, pakai kelas .reason dari halaman utama jika sesuai. Prinsipnya: tempat tidur lebih murah daripada hotel ditambah satu malam, jendela adalah bagian dari kamar, dan perjalanan lambat memang tujuannya. Tiap prinsip punya label mono dan paragraf pendek.
3. Linimasa singkat dengan tiga tonggak memakai label relatif seperti "Year one", "Year three", dan "This winter", bukan tanggal pasti yang dibuat-buat. Ceritakan layanan malam pertama, rute kedua yang ditambahkan, dan jadwal musim dingin saat ini.
4. Daftar "Where we go" berisi kota-kota yang sudah disebut di halaman utama: Lisbon, Paris, Vienna, Prague, Milan, dan Copenhagen. Buat sebagai daftar tipografi sederhana, bukan peta atau penghitung.
5. CTA penutup ke contact.html dengan label "Get in touch".

Jangan buat foto tim, nama staf, alamat kantor selain London, atau jumlah penumpang. Jangan menjalankan perintah git apa pun. Setelah selesai, sebutkan file yang Anda buat dan cara melihat pratinjau halaman secara lokal.
```

### 7. Kontak dan pemesanan (Serli)

```text
CONTEXT
Anda berkontribusi pada website statis kecil di folder ini: situs demo untuk "Nocturne", sebuah perusahaan kereta tidur fiktif. File index.html dan styles.css sudah disiapkan sebelumnya. Baca KEDUA file terlebih dahulu dan samakan persis.

Sistem desain yang harus dipakai ulang:
- Font dimuat di <head> dari Google Fonts: Syne untuk judul, DM Sans untuk teks isi, IBM Plex Mono untuk label, jam, dan data.
- Variabel CSS di styles.css: --ink #171b3d, --ink-deep #0d1030, --page #f6f8fc, --panel #e8edf6, --paper #ffffff, --slate #4d5375, --line #ccd3e2, --brass #f0a93b. Pakai variabel tersebut, jangan menciptakan warna baru.
- Kelas yang sudah ada dan harus dipakai ulang: .eyebrow, .section-lede, .btn, .btn-solid, .btn-brass, .text-link, .site-header, .site-footer, .strip-inner.
- Salin <head>, header, dan footer dari index.html ke halaman baru Anda agar semua halaman tampak seperti satu website yang sama. Pertahankan ketujuh tautan navigasi. Di halaman Anda saja, hapus label "soon" dari setiap tautan ke halaman Contact (header, menu mobile, dan footer). Jangan edit index.html.
- Teks antarmuka tetap dalam bahasa Inggris agar konsisten dengan halaman utama. Contoh kalimat di bawah sudah dalam bahasa Inggris.

ATURAN FILE YANG KETAT
- Buat HANYA contact.html dan, jika perlu gaya khusus halaman, contact.css. Hubungkan contact.css setelah styles.css di <head>.
- JANGAN ubah index.html atau styles.css. Ini membuat setiap pull request bebas konflik.
- Tanpa framework, tanpa UI kit CDN, tanpa atribut style inline. CSS eksternal saja.

ATURAN KUALITAS
- Responsif hingga 360px: tidak ada overflow horizontal, tidak ada teks terpotong, target sentuh minimal 44px.
- Pertahankan gaya fokus keyboard yang sudah didefinisikan secara global dan hormati prefers-reduced-motion.
- Jangan gunakan em dash. Jangan mengarang statistik, testimoni pelanggan, nama anggota tim, atau foto stok.
- Gunakan teks yang konkret dan sederhana dengan suara perusahaan kereta, bukan jargon pemasaran.
- Hindari label CTA umum seperti Get Started, Learn More, Explore, atau Discover.

TUGAS ANDA
Buat contact.html, halaman pemesanan dan kontak. Isinya:

1. Bagian pembuka dengan label kecil "Reservations", judul besar Syne seperti "Book a berth.", dan paragraf pembuka singkat.
2. Formulir kontak yang benar-benar berfungsi dengan kolom: nama lengkap, alamat email, rute pilihan berupa <select> yang berisi empat layanan N 102, N 214, N 308, dan N 416, tanggal perjalanan berupa input date, jumlah tamu, dan pesan. Tandai kolom penting sebagai required dan hubungkan setiap <label> dengan input lewat atribut for dan id.
3. Skrip <script> kecil di akhir body yang menangani event submit: cegah pengiriman bawaan, periksa kolom wajib sudah terisi, lalu tampilkan pesan sukses yang terlihat di dalam elemen dengan aria-live="polite". Jika ada kolom wajib yang kosong, beri fokus ke kolom itu dan tampilkan pesan error singkat. Tidak ada backend, jangan berpura-pura mengirim data lewat jaringan. Buat skripnya tetap pendek.
4. Blok detail kontak dengan tautan mailto ke hello@nocturne.example, kalimat "We reply within two working days" sebagai janji layanan, dan "London, United Kingdom" sebagai lokasi.
5. Catatan singkat "Before you write" yang meminta penumpang menyertakan kode rute dan tanggal perjalanan agar balasan lebih cepat.
6. CTA penutup ke routes.html dengan label "Check the timetable".

Formulir harus bisa dipakai hanya dengan keyboard, dengan fokus terlihat di setiap kolom dan tombol. Jangan menjalankan perintah git apa pun. Setelah selesai, sebutkan file yang Anda buat dan cara melihat pratinjau halaman secara lokal.
```

## Setelah ketujuh pull request di-merge

Pengajar menghapus label "soon" yang tersisa dari navigasi di `index.html`. Saat itu, semua tautan di situs menuju ke halaman yang benar-benar ada.
