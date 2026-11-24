# VPS Indonesia Murah: Mulai Rp 37.500 atau $2.99? Paket Mana yang Cukup untuk WordPress/WooCommerce, dan Biaya Apa yang Tidak Muncul di Halaman Harga

VPS murah di Indonesia mulai dari Rp 37.500 per bulan, dan angka itu benar-benar tercantum di halaman provider lokal. Uang segitu hanya membeli 1 core CPU, 1 GB RAM, dan sekitar 20 GB SSD. Blog WordPress ringan masih jalan; WooCommerce dengan beberapa plugin aktif akan cepat kehabisan RAM. Evoxt menawarkan jalur lain mulai $2.99 per bulan dengan node Jakarta, dan artikel ini membedah paketnya satu per satu, lalu menunjukkan biaya serta batasan yang jarang ditulis di halaman harga.

## Ringkasan: paket mana untuk siapa

> Sebagian besar pembaca cukup ambil **VM-1.5 ($6.95/bulan, 2 vCore, 2 GB RAM, 20 GB storage)**. Itu titik aman untuk WordPress dengan plugin standar. Kalau hanya memasang situs statis atau blog jarang update, VM-0.5 ($2.99) atau VM-0.75 ($4.99) sudah cukup. Untuk toko online kecil, mulai dari VM-2 ($11.99, 4 GB RAM).

Semua paket memakai KVM, mendapat alamat IPv4 sendiri, dan sudah termasuk backup mingguan off-site tanpa biaya tambahan menurut halaman resmi Evoxt. 👉 [Lihat paket VM-1.5 dan harga terbarunya](https://bit.ly/EvoXt)

## Semua paket Evoxt dan harganya

Harga di bawah diambil dari halaman resmi Evoxt. Semua angka dalam dolar AS dan ditagih per bulan; Evoxt menyediakan siklus penagihan dari bulanan sampai tiga tahun.

| Paket | vCPU / RAM | Storage | Harga | Tautan |
| --- | --- | --- | --- | --- |
| VM-0.5 | 1 vCore / 512 MB | 5 GB | $2.99/bln | [Pilih VM-0.5](https://bit.ly/EvoXt) |
| VM-0.75 | 1 vCore / 1 GB | — | $4.99/bln | [Pilih VM-0.75](https://bit.ly/EvoXt) |
| VM-1.5 | 2 vCore / 2 GB | 20 GB | $6.95/bln | [Pilih VM-1.5](https://bit.ly/EvoXt) |
| VM-2 | 2 vCore / 4 GB | 30 GB | $11.99/bln | [Pilih VM-2](https://bit.ly/EvoXt) |
| VM-3 | 4 vCore / 4 GB | 30 GB | $14.99/bln | [Pilih VM-3](https://bit.ly/EvoXt) |
| VM-6 | 8 vCore / 8 GB | 60 GB | $29.99/bln | [Pilih VM-6](https://bit.ly/EvoXt) |
| VM-8 | 8 vCore / 16 GB | 80 GB | $47.99/bln | [Pilih VM-8](https://bit.ly/EvoXt) |

Kapasitas storage VM-0.75 tidak tercantum pada kutipan halaman resmi yang bisa diakses; konfirmasi angkanya di halaman order sebelum membayar. Tipe storage tidak ditulis eksplisit di halaman paket, tetapi uji pihak ketiga yang membeli instance Jakarta pada Agustus 2025 melaporkan NVMe SSD dalam konfigurasi RAID10, prosesor AMD EPYC seri 9004, dan jaringan melalui AS149440.

Ada dua hal yang membuat struktur harga Evoxt berbeda dari kebanyakan provider lokal. Pertama, resource bisa ditambah satuan tanpa ganti paket: 1 vCore tambahan $3/bulan, 1 GB RAM tambahan $2/bulan, 1 IP tambahan $3/bulan, dan transfer tambahan $3/TB untuk jaringan Standard. Kedua, backup mingguan off-site sudah termasuk, bukan add-on berbayar.

Metode pembayaran yang diterima: kartu kredit, kartu debit, PayPal, Bitcoin, dan USDt Tron. Untuk pembaca yang tidak punya kartu kredit, PayPal dan crypto jadi jalan masuk utama.

## Harga murah itu sebenarnya dapat apa

Bandingkan angka dollar dengan harga rupiah di pasar lokal, karena selisihnya menjelaskan mengapa "murah" perlu didefinisikan ulang.

Kenceng Solusindo mencantumkan VPS Linux 1 seharga Rp 50.000 per bulan dengan 1 core CPU, 1 GB RAM, 20 GB SSD, dan kuota bandwidth 1 TB. Naik ke Rp 70.000, RAM menjadi 2 GB dengan storage tetap 20 GB. Rumahweb mengklaim harga mulai Rp 50.000, tetapi tabel paket di halaman yang sama menampilkan paket terendah Rp 120.000 untuk 1 vCPU, 2 GB RAM, dan 40 GB SSD. Herza Cloud menawarkan titik masuk Rp 37.500 per bulan.

Polanya jelas: Rp 50.000 membeli 1 GB RAM, dan Rp 120.000 baru membeli 2 GB RAM dengan storage dua kali lipat. VM-1.5 Evoxt berada di antara dua titik itu dengan 2 vCore dan 2 GB RAM seharga $6.95.

Pertanyaan yang lebih berguna: berapa RAM yang benar-benar dipakai WordPress? Instalasi WordPress bersih dengan tema ringan dan tiga sampai lima plugin biasanya menempati 300–500 MB. Panel seperti cPanel menambah beban sendiri. WooCommerce dengan katalog produk, plugin pembayaran, dan cache menambah 200–400 MB lagi, belum termasuk MySQL. Di sinilah 1 GB RAM mulai bermasalah: bukan langsung mati, tapi swap aktif dan waktu muat halaman naik.

Untuk situs statis, blog yang jarang diubah, atau server API kecil, VM-0.5 dengan 512 MB sudah cukup asal tidak memasang panel berat. Untuk WordPress biasa, VM-1.5 adalah batas bawah yang masuk akal. Untuk WooCommerce, VM-2 dengan 4 GB memberi ruang untuk database dan cache tanpa langsung menyentuh swap.

## Batasan yang tidak tertulis di halaman harga

Halaman harga biasanya hanya menampilkan CPU, RAM, storage, dan bandwidth. Beberapa ketentuan yang menentukan pengalaman pemakaian justru ada di FAQ atau syarat layanan.

**Port 25 ditutup secara default.** Rumahweb menyatakan port 25 pada VPS ditutup untuk mencegah penyalahgunaan spam, dan pengguna yang memang mengirim email harus mengirim permintaan whitelist ke tim teknis untuk diverifikasi. Kalau Anda berencana menjalankan mail server atau mengirim email transaksional langsung dari VPS, ini perlu dikonfirmasi sebelum memesan, termasuk untuk Evoxt yang ketentuan Acceptable Use Policy-nya tidak tercantum di halaman paket.

**Larangan VPN dan proxy berbeda antar provider.** Kenceng Solusindo menulis tegas bahwa layanannya tidak diperbolehkan untuk VPN, v2ray, tunneling, atau proxy. Halaman FAQ Evoxt memuat pertanyaan "Can I run a personal VPN server?" tetapi jawabannya tidak ikut tampil di kutipan yang bisa diakses, jadi jangan menganggap VPN otomatis diizinkan. Cek kebijakan penggunaan sebelum membeli kalau VPN adalah tujuan utamanya.

**Bandwidth "unlimited" punya rem.** Kenceng menyebut kuota bandwidth, dan jika terlampaui kecepatan diturunkan menjadi 8 Mbps sampai periode pembayaran berikutnya. Herza menyebut unlimited transfer dengan fair use. Tidak ada yang benar-benar tanpa batas; yang berbeda hanya cara penegakannya.

**VPS tidak selalu bisa dipindah antar-zone.** Rumahweb menyatakan VPS tidak dapat dimigrasikan antar availability zone; memindahkan beban kerja berarti membeli instance baru di zone tujuan dan memindahkan data sendiri.

**Refund bukan hal biasa.** Exabytes menulis "NO REFUND untuk pembelian produk VPS" dan biaya terminasi dihitung 100% dari sisa periode prabayar. Kebijakan refund Evoxt tidak tercantum di halaman paket yang bisa diakses, jadi tanyakan lewat kanal resminya sebelum membayar beberapa bulan sekaligus.

**Harga belum tentu termasuk pajak.** Exabytes mencantumkan bahwa harga belum termasuk PPN. Untuk pembelian dari Indonesia, ini mengubah total di invoice.

## Unmanaged vs managed: biaya sebenarnya

Semua paket VPS murah yang dibahas di sini bersifat unmanaged. Provider menjaga server tetap menyala dan jaringan tetap jalan; instalasi, konfigurasi, patch keamanan, dan pemulihan jadi tanggung jawab pengguna.

Kalau Anda tidak ingin menangani itu sendiri, biaya naik signifikan. Rumahweb menyediakan paket Managed Service seharga Rp 250.000 per bulan di luar lisensi cPanel. Exabytes menawarkan Pro Management Plan Rp 450.000 per bulan. Lisensi cPanel dan Plesk dihitung terpisah di kedua provider, dan Jagoan Hosting juga mencatat bahwa sebagian panel memerlukan lisensi berbayar.

Hitung sendiri efeknya. VPS Rp 120.000 ditambah managed Rp 250.000 menjadi Rp 370.000 per bulan, lebih mahal daripada paket VPS Rp 245.000 yang sudah mendapat 2 vCPU dan 4 GB RAM tanpa jasa pengelolaan. Membeli paket lebih besar tidak menghilangkan kebutuhan mengelola server, tetapi memberi ruang lebih sebelum kehabisan resource. Kalau pekerjaan teknis bukan hal yang ingin Anda tangani, anggaran pengelolaan harus masuk hitungan sejak awal, bukan ditambahkan setelah server bermasalah.

👉 [Bandingkan paket Evoxt sebelum memutuskan](https://bit.ly/EvoXt)

## Lokasi server dan arti Tier 3/Tier 4

Node Jakarta penting untuk situs dengan pengunjung Indonesia karena latency dan Time to First Byte lebih rendah dibanding server di Singapura atau Amerika. Rumahweb juga menyebut sisi kepatuhan: data yang berada di yurisdiksi Indonesia memudahkan pemenuhan UU PDP.

Soal Tier, sertifikasi ini mengukur keandalan aspek mekanikal dan elektrikal datacenter, bukan uptime layanan yang dijanjikan provider. Rumahweb merinci Tier 3 menjamin keandalan 99,982% per tahun (sekitar 1,6 jam gangguan) dan Tier 4 menjamin 99,995% (sekitar 30 menit). Angka itu berlaku untuk sistem pendingin dan kelistrikan gedung, bukan untuk VPS Anda secara individual.

Evoxt tidak mempublikasikan tier datacenter Jakarta-nya di halaman paket. Yang bisa diverifikasi dari uji pihak ketiga adalah jalur jaringan ke JKT-IX, yang merupakan titik pertukaran yang dipakai ISP Indonesia agar trafik lokal tidak dibelokkan ke luar negeri.

## Perbandingan dengan provider lokal

Tabel berikut hanya memuat informasi yang tercantum di halaman masing-masing provider. Tanggal halaman berbeda-beda, jadi harga bisa sudah berubah saat Anda membaca ini.

| Provider | Harga mulai (sesuai halaman) | Virtualisasi | Storage | Catatan yang tercantum |
| --- | --- | --- | --- | --- |
| Herza Cloud | Rp 37.500/bln | KVM | Enterprise SSD RAID10 | Halaman menyebut jumlah zone dan region yang saling bertentangan; transfer unlimited dengan fair use |
| Kenceng Solusindo | Rp 50.000/bln | KVM | SSD RAID10 | Melarang VPN, v2ray, tunneling, proxy; bandwidth lebih dari kuota turun ke 8 Mbps |
| Rumahweb | Rp 50.000/bln (klaim); paket terendah di tabel Rp 120.000 | KVM | SSD | Port 25 ditutup default; managed Rp 250.000/bln; VPS tidak bisa pindah availability zone |
| Jagoan Hosting | Rp 100.000/bln | — | SSD atau NVMe | 2–24 vCore, 2–128 GB RAM; sebagian panel perlu lisensi berbayar |

Yang perlu dicatat dari tabel ini: harga mulai yang dipromosikan di bagian atas halaman sering tidak sama dengan paket termurah yang benar-benar bisa dipesan. Rumahweb adalah contoh paling jelas, dengan klaim Rp 50.000 tetapi tabel yang dimulai dari Rp 120.000. Selalu buka tabel paket, bukan banner.

## FAQ

**VPS Rp 50.000 bisa menjalankan WooCommerce?**
Secara teknis bisa diinstal, tetapi 1 GB RAM terlalu ketat untuk WooCommerce dengan plugin pembayaran, katalog produk, dan cache. Mulai dari 2 GB RAM, dan idealnya 4 GB kalau ada trafik bersamaan.

**Apa beda unmetered dan unlimited?**
Keduanya berarti tidak ada kuota angka yang dipotong di muka, tetapi tetap tunduk pada fair use atau penurunan kecepatan. Kenceng menurunkan ke 8 Mbps setelah kuota terlampaui; Herza memakai fair use. Baca bagian ketentuan, bukan hanya label di kartu paket.

**Perlu cPanel? Berapa lisensinya?**
cPanel dan Plesk tidak termasuk dalam paket VPS murah mana pun di tabel ini. Rumahweb dan Jagoan Hosting menyebut lisensi panel dijual terpisah. Kalau tidak familier dengan command line, tambahkan biaya lisensi ke anggaran, atau pilih panel gratis seperti CyberPanel atau Webmin yang didukung sebagian provider.

**Bisa install Windows?**
Evoxt menyediakan template Windows Server. Lisensi Windows tidak otomatis termasuk, jadi konfirmasi biayanya di halaman order sebelum memilih template tersebut.

**Bisa dipakai untuk VPN atau proxy?**
Kenceng melarang tegas. Untuk Evoxt, kebijakan penggunaan tidak tercantum di halaman paket yang bisa diakses, jadi tanyakan langsung. Jangan berasumsi semua VPS murah mengizinkan VPN.

**Apakah backup termasuk?**
Evoxt menyatakan backup mingguan off-site sudah termasuk tanpa biaya tambahan. Exabytes menyertakan backup mingguan dan satu snapshot, tetapi restore dan reload OS dikenakan biaya teknis tambahan. Periksa apakah restore gratis atau berbayar.

## Cara memilih

Aturan sederhananya:

- Situs statis, blog jarang update, server API kecil: VM-0.5 atau VM-0.75.
- WordPress dengan plugin standar: VM-1.5.
- WooCommerce, forum, atau aplikasi dengan koneksi bersamaan: VM-2 ke atas.
- Butuh bantuan mengelola server: tambahkan biaya managed Rp 250.000–450.000 per bulan ke total, atau pilih provider yang menyertakan pengelolaan.
- Butuh kirim email dari VPS: konfirmasi status port 25 sebelum membayar.
- Butuh VPN atau proxy: pastikan kebijakan penggunaan mengizinkannya.

Tiga hal yang perlu dikonfirmasi di halaman order sebelum membayar: siklus penagihan yang dipilih (bulanan atau tahunan), harga perpanjangan setelah periode pertama, dan kebijakan refund. Tidak ada satu pun provider di artikel ini yang mencantumkan harga perpanjangan di halaman paket, jadi jangan mengasumsikan harga bulan pertama berlaku selamanya.

👉 [Mulai dari paket terkecil Evoxt dan cek harga terbarunya di halaman order](https://bit.ly/EvoXt)
