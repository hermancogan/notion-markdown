---
title: "7 LAYER OSI & TCP/IP LAYERS"
slug: "7-layer-osi-tcpip-layers"
excerpt: "PENDAHULUAN --- Ketika kamu mengirim pesan ke teman melalui aplikasi chat, atau membuka video di YouTube, tahukah kamu ada banyak proses yang terjadi di balik layar? Data mu harus melewati berbagai “s…"
categories: ["Networking"]
tags: ["SMK", "Komputer"]
created_time: "01.11 27-01-26"
last_edited_time: "2026-01-26T17:13:00.000Z"
url: "https://www.notion.so/7-layer-osi-tcpip-layers-2f4f2e85b5918056b732dff5c633227f"
author: ["Sultan"]
contributor: ["Goks"]
---

## PENDAHULUAN


---

Ketika kamu mengirim pesan ke teman melalui aplikasi chat, atau membuka video di YouTube, tahukah kamu ada banyak proses yang terjadi di balik layar? Data mu harus melewati berbagai “stasiun” sebelum sampai ke tujuan. Dua model yang menjelaskan “stasiun-stasiun” ini adalah **OSI Model** dan **TCP/IP Model**.

**Analogi Sederhana:**
Bayangkan mengirim paket ke teman di kota lain. Paket mu harus:
1. Dikemas rapi (ditambah alamat, nama pengirim)
2. Diserahkan ke kantor pos
3. Diangkut ke pusat distribusi regional
4. Diangkut ke kota tujuan
5. Diantar oleh kurir lokal
6. Diterima dan dibuka teman mu

Dalam jaringan komputer, data juga mengalami perjalanan serupa! Inilah yang dijelaskan oleh **OSI Model** (dengan 7 tahap) dan **TCP/IP Model** (dengan 4 tahap).


---

## BAB 1: MEMAHAMI OSI MODEL (7 LAYER)

### 1.1 Apa itu OSI Model?

**OSI** singkatan dari **Open Systems Interconnection**. Ini adalah model referensi yang menjelaskan bagaimana data bergerak dari satu perangkat ke perangkat lain dalam jaringan komputer.

**Karakteristik OSI Model:**
- ✓ Memiliki **7 lapisan** yang berbeda
- ✓ Model ini lebih **teoritis** (dibuat sebagai standar, bukan dari protokol yang sudah ada)
- ✓ Membantu **memahami** dan **mendiagnosis** masalah jaringan
- ✓ Setiap lapisan memiliki **fungsi spesifik** dan terisolasi
- ✓ Lapisan berkomunikasi dengan lapisan di atas dan di bawahnya


---

### 1.2 TUJUH LAPISAN OSI MODEL

Untuk mengingat urutan 7 lapisan, gunakan akronim: **“Please Do Not Throw Sausage Pizza Away”**
- **P**hysical (Lapisan 1)
- **D**ata Link (Lapisan 2)
- **N**etwork (Lapisan 3)
- **T**ransport (Lapisan 4)
- **S**ession (Lapisan 5)
- **P**resentation (Lapisan 6)
- **A**pplication (Lapisan 7)


---

### LAPISAN 1: PHYSICAL LAYER (Lapisan Fisik)

**Apa yang dilakukan?**
Lapisan ini menangani **transmisi data dalam bentuk bit** (0 dan 1) melalui media fisik.

**Analogi:**
Seperti kabel USB yang menghubungkan keyboard ke komputer. Lapisan ini adalah “kabel” yang membawa arus listrik.

**Perangkat yang bekerja di sini:**
- Kabel jaringan (Ethernet, fiber optik)
- Hub jaringan
- Wireless transmitter (pembuat sinyal WiFi)
- Konektor jaringan

**Protokol:**
- Ethernet
- USB
- Kabel coaxial, twisted pair

**Satuan Data:** Bit (0 dan 1)

**Pertanyaan untuk Ingat:**
“Bagaimana data dikirim secara FISIK?” → Jawabannya: Melalui sinyal listrik di kabel atau sinyal radio di udara!


---

### LAPISAN 2: DATA LINK LAYER (Lapisan Tautan Data)

**Apa yang dilakukan?**
Lapisan ini mengatur **pengiriman data antar perangkat DALAM JARINGAN YANG SAMA** (jaringan lokal). Ia menggunakan **MAC Address** untuk mengidentifikasi perangkat.

**Analogi:**
Seperti sistem pengiriman lokal di satu kampus. Paket dikirim berdasarkan nomor ruangan (MAC Address), bukan alamat kota (IP Address).

**Fungsi Utama:**
- Membagi data menjadi **frame** (kotak-kotak data)
- Menambahkan MAC Address pengirim dan penerima
- Mendeteksi dan memperbaiki **error** dalam transmisi

**Perangkat yang bekerja di sini:**
- Switch jaringan
- Network Interface Card (NIC) / Kartu jaringan

**Protokol:**
- MAC (Media Access Control)
- ARP (Address Resolution Protocol) - untuk mencari MAC Address dari IP Address
- Ethernet

**Satuan Data:** Frame

**Contoh MAC Address:** `00:1A:2B:3C:4D:5E`

**Pertanyaan untuk Ingat:**
“Bagaimana cara menemukan perangkat di jaringan yang sama?” → Jawabannya: Gunakan MAC Address!


---

### LAPISAN 3: NETWORK LAYER (Lapisan Jaringan)

**Apa yang dilakukan?**
Lapisan ini menangani **routing** (mencari jalur) dan **pengalamatan IP**. Ia menentukan bagaimana data bepergian dari jaringan satu ke jaringan lain.

**Analogi:**
Seperti sistem alamat kota/negara. Ketika kamu mengirim paket ke kota lain, layanan pos perlu tahu jalur mana yang paling cepat melalui peta.

**Fungsi Utama:**
- Menentukan **IP Address** pengirim dan penerima
- Menemukan **jalur terbaik** (routing) untuk pengiriman data
- Memecah data besar menjadi **paket** yang lebih kecil
- Menentukan routing antar jaringan

**Perangkat yang bekerja di sini:**
- Router
- Layer 3 Switch
- Firewall jaringan (network firewall)

**Protokol:**
- **IP** (Internet Protocol) - IPv4 dan IPv6
- **ICMP** (untuk ping dan error reporting)
- **RIP** dan **OSPF** (routing protocols)

**Satuan Data:** Packet

**Contoh IP Address:** `192.168.1.1` atau `8.8.8.8`

**Pertanyaan untuk Ingat:**
“Bagaimana data menemukan jalur ke jaringan lain?” → Jawabannya: Menggunakan IP Address dan routing!


---

### LAPISAN 4: TRANSPORT LAYER (Lapisan Transportasi)

**Apa yang dilakukan?**
Lapisan ini bertanggung jawab atas **pengiriman data end-to-end** (dari aplikasi awal ke aplikasi tujuan) dengan cara yang **andal atau cepat**.

**Analogi:**
Seperti memilih antara mengirim paket dengan kurir kilat (cepat tapi ada risiko), atau dengan kurir biasa yang lebih berhati-hati (lambat tapi aman).

**Fungsi Utama:**
- Memecah data dari lapisan aplikasi menjadi **segment**
- Menentukan **port** komunikasi (port adalah “pintu” untuk aplikasi)
- Mengatur **kecepatan dan jumlah** data yang dikirim
- Memastikan **reliabilitas** pengiriman atau memprioritaskan **kecepatan**

**Protokol Utama:**
- **TCP** (Transmission Control Protocol)
- Andal (data sampai dengan pasti)
- Koneksi-oriented (harus handshake dulu)
- Lebih lambat
- Digunakan untuk: Email, HTTP/HTTPS, File transfer

- **UDP** (User Datagram Protocol)
  - Cepat tapi tidak andal
  - Connectionless (langsung kirim tanpa handshake)
  - Lebih cepat
  - Digunakan untuk: Streaming video, online gaming, VoIP
**Perangkat yang bekerja di sini:**
- Gateway
- Firewall (layer 4)

**Satuan Data:** Segment (TCP) atau Datagram (UDP)

**Contoh Port:**
- Port 80 untuk HTTP
- Port 443 untuk HTTPS
- Port 25 untuk SMTP (email)

**Pertanyaan untuk Ingat:**
“Bagaimana cara memastikan data sampai dengan selamat?” → Jawabannya: Gunakan TCP untuk andal, UDP untuk kecepatan!


---

### LAPISAN 5: SESSION LAYER (Lapisan Sesi)

**Apa yang dilakukan?**
Lapisan ini **mengelola percakapan** (session) antara dua perangkat. Ia memastikan percakapan itu dimulai dengan baik, berlangsung, dan ditutup dengan benar.

**Analogi:**
Seperti petugas di sebuah restoran yang mengatur ketika pelanggan datang, duduk, diberi menu, memesan, makan, membayar, dan pergi. Setiap tahap memiliki prosesnya.

**Fungsi Utama:**
- **Membangun koneksi** antar perangkat (setup)
- **Mempertahankan koneksi** (maintenance) selama komunikasi berlangsung
- **Mengakhiri koneksi** dengan rapi (termination)
- Menangani **authentication** (verifikasi siapa yang terhubung)
- Mengatur **synchronization** (sinkronisasi) data

**Protokol:**
- **NetBIOS** - untuk komunikasi lokal
- **PPTP** (Point-to-Point Tunneling Protocol)
- **RPC** (Remote Procedure Call)

**Satuan Data:** Data (dikelola dari session)

**Contoh Situasi:**
Ketika kamu login ke email:
1. **Session Layer** membangun koneksi dengan server email
2. Kamu mengirim username dan password
3. Server menerima dan memverifikasi
4. Percakapan tetap terbuka selama kamu membaca email
5. Ketika kamu logout, Session Layer menutup koneksi dengan rapi

**Pertanyaan untuk Ingat:**
“Bagaimana dua perangkat memulai, menjaga, dan mengakhiri percakapan?” → Jawabannya: Melalui manajemen session!


---

### LAPISAN 6: PRESENTATION LAYER (Lapisan Presentasi)

**Apa yang dilakukan?**
Lapisan ini **mengubah format data** sehingga dapat dipahami oleh aplikasi penerima. Ia juga menangani **enkripsi** dan **kompresi**.

**Analogi:**
Seperti seorang penerjemah yang mengubah data dari format “bahasa pengirim” ke format “bahasa penerima” agar sama-sama mengerti.

**Fungsi Utama:**
- **Encoding/Decoding** - mengubah format karakter (ASCII, Unicode)
- **Encryption/Decryption** - mengenkripsi data agar aman saat dalam perjalanan
- **Compression/Decompression** - mengecilkan ukuran data agar lebih cepat dikirim
- Memastikan data dalam format yang dimengerti aplikasi penerima

**Protokol:**
- **TLS/SSL** (untuk enkripsi HTTPS)
- **MIME** (Multipurpose Internet Mail Extensions) - untuk email
- **JPEG, PNG, GIF** - format gambar
- **MP3, MPEG** - format multimedia

**Contoh Transformasi:**
- Teks biasa → Teks terenkripsi (keamanan)
- File besar → File yang dikompres (untuk transfer lebih cepat)
- Data dalam format A → Data dalam format B yang dimengerti sistem penerima

**Pertanyaan untuk Ingat:**
“Bagaimana data diubah formatnya agar kedua perangkat saling memahami?” → Jawabannya: Melalui encoding, encryption, dan compression!


---

### LAPISAN 7: APPLICATION LAYER (Lapisan Aplikasi)

**Apa yang dilakukan?**
Lapisan ini adalah **yang terdekat dengan pengguna**. Di sini, aplikasi (seperti browser, email, game online) berkomunikasi dengan jaringan.

**Analogi:**
Seperti kasir di sebuah toko. Kasir adalah yang berinteraksi langsung dengan pelanggan. Pelanggan tidak perlu tahu bagaimana sistem logistik bekerja; mereka hanya perlu berbicara dengan kasir.

**Fungsi Utama:**
- Menyediakan **layanan jaringan** kepada aplikasi
- Mengidentifikasi **sumber daya** yang tersedia di jaringan
- Mengenkripsi data (dari perspektif aplikasi)
- Melakukan **authentication dan authorization**
- Menangani **data formatting** untuk tampilan pengguna

**Protokol (yang mungkin kamu gunakan setiap hari):**
- **HTTP/HTTPS** - untuk browsing web
- **FTP** - untuk transfer file
- **SMTP** - untuk mengirim email
- **POP3/IMAP** - untuk menerima email
- **DNS** - untuk menerjemahkan nama domain (google.com) ke IP Address
- **DHCP** - untuk memberikan IP Address otomatis
- **Telnet** - untuk remote login
- **SSH** - untuk secure remote login

**Contoh Aplikasi:**
- Google Chrome (web browser)
- Gmail (email client)
- WhatsApp (messaging)
- YouTube (streaming video)
- Zoom (video conferencing)

**Pertanyaan untuk Ingat:**
“Aplikasi apa yang kamu gunakan untuk berkomunikasi di internet?” → Jawabannya: HTTP untuk browsing, SMTP untuk email, dan sebagainya!


---

### 1.3 RINGKASAN 7 LAYER OSI


| Layer | Nama | Fungsi | Analogi | Contoh Protocol |
| --- | --- | --- | --- | --- |
| 7 | Application | Interface untuk aplikasi pengguna | Kasir di toko | HTTP, FTP, SMTP, DNS |
| 6 | Presentation | Encoding, enkripsi, kompresi | Penerjemah | TLS/SSL, MIME, JPEG |
| 5 | Session | Mengelola sesi/percakapan | Petugas restoran | NetBIOS, PPTP, RPC |
| 4 | Transport | Pengiriman end-to-end | Kurir dengan pilihan kilat/biasa | TCP, UDP |
| 3 | Network | Routing dan IP addressing | Sistem alamat kota | IP, ICMP, RIP |
| 2 | Data Link | Pengiriman lokal dengan MAC Address | Sistem pengiriman kampus | MAC, ARP, Ethernet |
| 1 | Physical | Transmisi bit melalui media fisik | Kabel dan sinyal listrik | Ethernet cable, WiFi |


---

## BAB 2: MEMAHAMI TCP/IP MODEL (4 LAYER)

### 2.1 Apa itu TCP/IP Model?

**TCP/IP** adalah model jaringan yang lebih **praktis dan real** dibandingkan OSI. Ini adalah model yang BENAR-BENAR digunakan di internet hari ini!

**Karakteristik TCP/IP Model:**
- ✓ Memiliki **4 lapisan** (lebih sederhana dari OSI)
- ✓ Model ini **berbasis protokol** yang sudah berfungsi (TCP dan IP)
- ✓ Dikembangkan oleh **Departemen Pertahanan Amerika** (DoD)
- ✓ Lebih **reliable** (andal) dalam pengiriman data
- ✓ **Standard actual** yang digunakan internet modern


---

### 2.2 EMPAT LAPISAN TCP/IP MODEL

Untuk mengingat urutan, gunakan: **“Can I Take Applications?”**
- **C**an = Network Access/Link Layer
- **I** = Internet Layer
- **T**ake = Transport Layer
- **A**pplications = Application Layer


---

### LAPISAN 1: NETWORK ACCESS LAYER (Lapisan Akses Jaringan)

**Apa yang dilakukan?**
Lapisan ini menangani **transmisi fisik data** dan **pengiriman lokal dalam jaringan yang sama**. Ini adalah **kombinasi dari Lapisan Fisik dan Data Link OSI**.

**Analogi:**
Seperti kantor pos lokal yang mengirim surat hanya ke lingkungan sekitar.

**Fungsi Utama:**
- Mengubah paket IP menjadi **frame** (format yang bisa dikirim fisik)
- Menangani **transmisi fisik** data (bit dan signal)
- Melakukan **MAC Address** mapping (IP ke MAC)
- Mendeteksi dan menangani **error** dalam transmisi lokal
- Mengatur akses ke media fisik (kabel, WiFi)

**Protokol:**
- **Ethernet** - untuk jaringan kabel
- **WiFi (802.11)** - untuk jaringan wireless
- **PPP** (Point-to-Point Protocol) - untuk dial-up
- **Frame Relay**

**Perangkat:**
- Network Interface Card (NIC)
- Ethernet cables
- WiFi adapter
- Modem
- Switch

**Satuan Data:** Frame

**Pertanyaan untuk Ingat:**
“Bagaimana data dikirim secara FISIK dan LOKAL?” → Jawabannya: Melalui Ethernet, WiFi, dan perangkat fisik!


---

### LAPISAN 2: INTERNET LAYER (Lapisan Internet)

**Apa yang dilakukan?**
Lapisan ini menangani **routing antar jaringan** dan **IP addressing**. Data disini disebut **packet**.

**Analogi:**
Seperti sistem kereta api nasional yang menghubungkan kota-kota di seluruh negara. Kereta mengetahui jalur mana yang harus diambil.

**Fungsi Utama:**
- Menentukan **IP Address** pengirim dan penerima
- Melakukan **routing** (mencari jalur terbaik)
- Memecah data besar menjadi **paket** (jika perlu)
- Mengirim paket melalui berbagai jaringan menuju tujuan
- Menangani **error reporting** (ICMP)

**Protokol Utama:**
- **IP (Internet Protocol)**
- IPv4 (192.168.1.1)
- IPv6 (2001:0db8:85a3::8a2e:0370:7334)
- **ICMP** (Internet Control Message Protocol)
- Protokol untuk ping
- Laporan error
- **IGMP** (Internet Group Management Protocol)
- Untuk multicast

**Perangkat:**
- Router
- Layer 3 Switch

**Satuan Data:** Packet

**Contoh Proses Routing:**
1. Datamu memiliki IP tujuan: 8.8.8.8 (Google DNS)
2. Router lokal mu melihat IP ini BUKAN dari jaringan lokal
3. Router mengirim packet ke router “tetangga” yang lebih dekat ke 8.8.8.8
4. Proses ini berulang sampai paket mencapai 8.8.8.8

**Pertanyaan untuk Ingat:**
“Bagaimana paket dikirim dari satu jaringan ke jaringan lain?” → Jawabannya: Melalui IP addressing dan routing!


---

### LAPISAN 3: TRANSPORT LAYER (Lapisan Transportasi)

**Apa yang dilakukan?**
Sama seperti OSI Layer 4, lapisan ini menangani **pengiriman end-to-end** dengan dua pilihan protokol: **TCP** (andal) atau **UDP** (cepat).

**Analogi:**
Seperti memilih antara paket yang diasuransikan (TCP - pasti sampai tapi mahal/lambat) atau paket tanpa asuransi (UDP - cepat tapi ada risiko).

**Fungsi Utama:**
- Memilih antara **TCP atau UDP** berdasarkan kebutuhan aplikasi
- Menangani **port** (pintu aplikasi)
- Mengatur **flow control** (kecepatan data)
- Melakukan **error checking dan correction** (untuk TCP)
- Mengelola **segmen data** dari aplikasi

**Protokol:**
- **TCP** (Transmission Control Protocol)
- Connection-oriented
- Andal (data pasti sampai)
- Contoh: HTTP, SMTP, FTP, SSH, Telnet

- **UDP** (User Datagram Protocol)
  - Connectionless
  - Cepat tapi tidak andal
  - Contoh: DNS, VoIP, Streaming video, Online gaming
**Satuan Data:** Segment (TCP) atau Datagram (UDP)

**Contoh Port Umum:**
- Port 80: HTTP (web)
- Port 443: HTTPS (web secure)
- Port 21: FTP (file transfer)
- Port 25: SMTP (send email)
- Port 110: POP3 (receive email)
- Port 53: DNS (domain name)
- Port 22: SSH (secure login)

**Pertanyaan untuk Ingat:**
“Bagaimana memilih antara pengiriman yang andal atau cepat?” → Jawabannya: TCP untuk andal, UDP untuk cepat!


---

### LAPISAN 4: APPLICATION LAYER (Lapisan Aplikasi)

**Apa yang dilakukan?**
Lapisan ini menyediakan **layanan jaringan langsung kepada aplikasi pengguna**. Ini adalah **kombinasi OSI Layer 5, 6, dan 7**.

**Analogi:**
Seperti toko yang melayani pelanggan dengan berbagai layanan: kasir, sistem pembayaran, wrapping hadiah, dll.

**Fungsi Utama:**
- Menyediakan **layanan jaringan** untuk aplikasi
- Mengidentifikasi **sumber daya** yang tersedia
- Melakukan **resource sharing**
- Menyediakan **user interface** untuk komunikasi jaringan
- Menangani **data compression, encryption, dan translation**

**Protokol Utama:**


| Protokol | Fungsi | Port | Contoh Penggunaan |
| --- | --- | --- | --- |
| **HTTP/HTTPS** | Transfer halaman web | 80/443 | Browsing website |
| **FTP** | Transfer file | 21 | Download/upload file |
| **SMTP** | Mengirim email | 25 | Kirim email |
| **POP3** | Menerima email | 110 | Terima email |
| **IMAP** | Menerima dan sinkronisasi email | 143 | Terima email (modern) |
| **DNS** | Menerjemahkan domain ke IP | 53 | google.com → 142.251.x.x |
| **DHCP** | Memberikan IP otomatis | 67/68 | IP address otomatis di WiFi |
| **SSH** | Secure remote login | 22 | Login server dengan aman |
| **Telnet** | Remote login (tidak aman) | 23 | Remote login (legacy) |
| **SNMP** | Network management | 161 | Monitor perangkat jaringan |

**Contoh Aplikasi:**
- Web browsers (Chrome, Firefox)
- Email clients (Gmail, Outlook)
- File transfer (FTP clients)
- Remote access (SSH, RDP)
- Video streaming (YouTube)
- Online gaming
- VoIP (WhatsApp, Skype)

**Pertanyaan untuk Ingat:**
“Aplikasi apa yang kamu gunakan untuk internet?” → Jawabannya: Semua aplikasi yang menggunakan protokol di layer 4 ini!


---

### 2.3 RINGKASAN 4 LAYER TCP/IP


| Layer | Nama | Fungsi | Analogi | Contoh Protocol |
| --- | --- | --- | --- | --- |
| 4 | Application | Layanan untuk aplikasi pengguna | Toko lengkap | HTTP, FTP, SMTP, DNS |
| 3 | Transport | Pengiriman end-to-end (andal/cepat) | Kurir kilat atau biasa | TCP, UDP |
| 2 | Internet | Routing dan IP addressing | Kereta antar kota | IP, ICMP |
| 1 | Network Access | Transmisi fisik dan lokal | Kantor pos lokal | Ethernet, WiFi, PPP |


---

## BAB 3: PERBANDINGAN OSI vs TCP/IP

### 3.1 Tabel Perbandingan Detail


| Aspek | OSI Model | TCP/IP Model |
| --- | --- | --- |
| **Jumlah Layer** | 7 lapisan | 4 lapisan |
| **Jenis Model** | Teoritis (dibuat sebagai standar) | Praktis (dari protokol yang sudah ada) |
| **Pengembangan** | Distandarkan oleh ISO | Dikembangkan DoD (Departemen Pertahanan US) |
| **Kompleksitas** | Lebih kompleks | Lebih sederhana |
| **Penerapan** | Jarang diterapkan sepenuhnya | Digunakan di internet nyata |
| **Diagnosis** | Lebih mudah untuk troubleshooting | Lebih fokus pada protokol spesifik |
| **Layer 1-2** | Physical + Data Link (terpisah) | Network Access (gabungan) |
| **Layer 3** | Network | Internet (sama fungsi) |
| **Layer 4** | Transport | Transport (sama fungsi) |
| **Layer 5-7** | Session, Presentation, Application | Application (gabungan) |
| **Reliabilitas** | Bervariasi per layer | Lebih andal (khususnya TCP) |

### 3.2 Perbandingan Tingkat Lanjutan

**Dalam OSI, 7 lapisan memiliki **fungsi yang sangat terspesialisasi**:**
- Session hanya mengelola koneksi
- Presentation hanya mengurus format data
- Application hanya menyediakan layanan

**Dalam TCP/IP, fungsi ini **digabungkan** di Application Layer:**
- Format data, koneksi, dan layanan dihandle bersama

**Analogi:**
- OSI seperti rumah sakit dengan dokter spesialis (setiap dokter fokus pada satu bagian tubuh)
- TCP/IP seperti klinik kecil (dokter umum menangani berbagai penyakit)


---

## BAB 4: ALUR DATA MELALUI OSI DAN TCP/IP

### 4.1 Perjalanan Data (Dari Pengirim ke Penerima)

**Skenario:** Kamu mengirim email melalui Gmail

**Melalui OSI Model:**

```plain text

```

**Melalui TCP/IP Model:**

```plain text

```

### 4.2 Istilah yang Penting Diingat

**PDU (Protocol Data Unit) - Satuan Data di Setiap Layer:**


| Layer | OSI | TCP/IP |
| --- | --- | --- |
| **Layer 7/4** | Data | Data |
| **Layer 6** | Data | Data |
| **Layer 5** | Data | Data |
| **Layer 4** | Segment (TCP) / Datagram (UDP) | Segment / Datagram |
| **Layer 3/2** | Packet | Packet |
| **Layer 2/1** | Frame | Frame |
| **Layer 1** | Bit | Bit |


---

## BAB 5: PENERAPAN PRAKTIS DI DUNIA NYATA

### 5.1 Troubleshooting Jaringan dengan OSI Model

Ketika jaringan kamu bermasalah, gunakan OSI untuk mencari tahu layer mana yang error:

**Masalah:** “Tidak bisa browsing web”

**Diagnosis Dari Bawah Ke Atas:**

1. **Layer 1 (Physical):** Apakah kabel ethernet terhubung? Apakah lampu jaringan menyala?
  - Solusi: Hubungkan kabel atau restart modem
1. **Layer 2 (Data Link):** Apakah komputer dapat berkomunikasi dengan router?
  - Cek: `ipconfig /all` (Windows) atau `ifconfig` (Mac/Linux)
  - Apakah ada MAC Address?
1. **Layer 3 (Network):** Apakah komputer memiliki IP Address yang valid?
  - Cek: IP address (192.168.x.x atau 10.x.x.x untuk lokal)
  - Coba ping router: `ping 192.168.1.1`
1. **Layer 4 (Transport):** Apakah port 80 (HTTP) atau 443 (HTTPS) terbuka?
  - Coba: `netstat -an` untuk melihat port yang aktif
1. **Layer 5 (Session):** Apakah session browser terbuka dengan baik?
  - Coba: Tutup browser dan buka lagi
1. **Layer 6 (Presentation):** Apakah data dikompres/enkripsi dengan benar?
  - Coba: Disable VPN jika sedang aktif
1. **Layer 7 (Application):** Apakah browser atau server web bermasalah?
  - Coba: Ganti browser atau cek status server
### 5.2 Contoh Protokol Nyata

**Ketika Kamu Membuka YouTube:**

```plain text

```


---

## BAB 6: SOAL LATIHAN DAN JAWABAN

### 6.1 SOAL PILIHAN GANDA

**1. Protokol apa yang digunakan untuk browsing web?**
A. SMTP
B. FTP
C. HTTP/HTTPS
D. DNS

**Jawaban: C***Penjelasan: HTTP/HTTPS adalah protokol Layer 7 (Application) untuk transfer halaman web.*


---

**2. MAC Address digunakan di layer OSI mana?**
A. Layer 1
B. Layer 2
C. Layer 3
D. Layer 4

**Jawaban: B***Penjelasan: MAC Address adalah identitas perangkat lokal, digunakan di Data Link Layer (Layer 2).*


---

**3. Protokol mana yang lebih andal untuk pengiriman data?**
A. UDP
B. TCP
C. IP
D. ICMP

**Jawaban: B***Penjelasan: TCP adalah connection-oriented dan memastikan semua data sampai dengan urutan benar.*


---

**4. Berapa jumlah layer dalam TCP/IP Model?**
A. 5 layer
B. 4 layer
C. 6 layer
D. 7 layer

**Jawaban: B***Penjelasan: TCP/IP Model memiliki 4 layer: Application, Transport, Internet, Network Access.*


---

**5. Perangkat apa yang bekerja di Layer 3 (Network Layer)?**
A. Switch
B. Hub
C. Router
D. Network Card

**Jawaban: C***Penjelasan: Router melakukan routing antar jaringan berdasarkan IP Address.*


---

**6. Lapisan apa yang menangani enkripsi dan kompresi data?**
A. Transport Layer
B. Session Layer
C. Presentation Layer
D. Application Layer

**Jawaban: C***Penjelasan: Presentation Layer (Layer 6 OSI) menangani encryption, compression, dan format data.*


---

**7. Port 25 digunakan untuk protokol apa?**
A. HTTP
B. SMTP
C. FTP
D. DNS

**Jawaban: B***Penjelasan: Port 25 adalah SMTP untuk mengirim email.*


---

**8. Apa singkatan dari IP?**
A. Internet Protocol
B. Internal Protocol
C. Inter Program
D. Internet Program

**Jawaban: A***Penjelasan: IP adalah Internet Protocol, digunakan untuk addressing antar jaringan.*


---

**9. Session Layer (Layer 5) bertanggung jawab untuk apa?**
A. Routing paket
B. Membuka dan menutup koneksi
C. Enkripsi data
D. Format data

**Jawaban: B***Penjelasan: Session Layer mengelola pembukaan, pemeliharaan, dan penutupan koneksi.*


---

**10. Protokol mana yang TIDAK termasuk dalam TCP/IP Application Layer?**
A. HTTP
B. ICMP
C. FTP
D. DNS

**Jawaban: B***Penjelasan: ICMP adalah protokol Internet Layer (Layer 2 TCP/IP), bukan Application Layer.*


---

### 6.2 SOAL URAIAN

**Soal 1: Jelaskan perbedaan antara TCP dan UDP!**

Jawaban:
- **TCP (Transmission Control Protocol):**
- Connection-oriented (harus handshake dulu)
- Andal (data pasti sampai dengan urutan benar)
- Lebih lambat
- Digunakan untuk: Email, Web, File transfer
- Overhead lebih besar

- **UDP (User Datagram Protocol):**
  - Connectionless (langsung kirim)
  - Tidak andal (mungkin ada data yang hilang)
  - Lebih cepat
  - Digunakan untuk: Video streaming, Gaming, VoIP
  - Overhead lebih kecil

---

**Soal 2: Sebutkan 5 protokol Application Layer dan fungsinya!**

Jawaban:
1. **HTTP/HTTPS** - Untuk browsing web (port 80/443)
2. **SMTP** - Untuk mengirim email (port 25)
3. **FTP** - Untuk transfer file (port 21)
4. **DNS** - Untuk menerjemahkan domain ke IP (port 53)
5. **SSH** - Untuk login remote yang aman (port 22)


---

**Soal 3: Apa yang terjadi ketika kamu mengirim file melalui email?**

Jawaban:
1. **Layer 7 (Application):** Email client membuat email dengan file attachment
2. **Layer 6 (Presentation):** File dikompres dan dienkripsi
3. **Layer 5 (Session):** Koneksi dengan server email dibuka
4. **Layer 4 (Transport):** Email dipecah menjadi segment, menggunakan TCP dan port 587
5. **Layer 3 (Network):** Segment dikemas paket dengan IP server email
6. **Layer 2 (Data Link):** Paket dibungkus frame dengan MAC router
7. **Layer 1 (Physical):** Frame dikirim melalui sinyal listrik
8. **Prosesnya berulang di sisi penerima dengan urutan terbalik**


---

**Soal 4: Mengapa TCP/IP lebih sering digunakan daripada OSI?**

Jawaban:
- TCP/IP adalah model yang **praktis dan berbasis protokol nyata** yang sudah berfungsi
- TCP/IP lebih **sederhana** (4 layer vs 7 layer)
- TCP/IP adalah **standar internet** yang sebenarnya digunakan
- OSI adalah model **teoritis** yang dibuat sebagai standar referensi
- TCP/IP lebih **fleksibel** dan **reliable** untuk implementasi nyata
- Internet modern **dibangun atas dasar TCP/IP**, bukan OSI


---

**Soal 5: Jika kamu tidak bisa terhubung ke internet, bagaimana cara troubleshooting menggunakan OSI Model?**

Jawaban:
1. **Layer 1:** Cek apakah kabel terhubung, lampu jaringan menyala
2. **Layer 2:** Cek apakah MAC Address terdeteksi (`ipconfig`)
3. **Layer 3:** Cek apakah IP Address valid (`ping 192.168.1.1`)
4. **Layer 4:** Cek apakah port terbuka dan layanan berjalan
5. **Layer 5:** Restart browser atau aplikasi
6. **Layer 6:** Disable encryption/compression jika ada masalah
7. **Layer 7:** Cek apakah website/server sedang down


---

## PENUTUP

### Ringkasan Penting

**7 Layer OSI:**
Dari bawah ke atas = Physical → Data Link → Network → Transport → Session → Presentation → Application

Cara ingat: **“Please Do Not Throw Sausage Pizza Away”**

**4 Layer TCP/IP:**
Dari bawah ke atas = Network Access → Internet → Transport → Application

Cara ingat: **“Can I Take Applications?”**

**Ingat:**
- OSI = Model teoritis untuk **memahami**
- TCP/IP = Model praktis yang **benar-benar digunakan** di internet

**Konsep Kunci:**
1. Data bergerak dari atas ke bawah saat dikirim, bawah ke atas saat diterima
2. Setiap layer menambahkan “header” (informasi kontrol) ke data
3. Setiap layer berkomunikasi dengan layer yang sama di perangkat lain
4. Pilih TCP untuk andal, UDP untuk cepat
5. Gunakan OSI untuk troubleshooting, TCP/IP untuk pemahaman internet real


---

### Daftar Pustaka

- Extrahop. (2024). “Understanding the OSI Model and OSI Layers in 2024”
- DataFlair. (2021). “TCP/IP Model - Layers and Architecture”
- Telkom University. (2025). “Perbedaan Model OSI dan TCP/IP dalam Jaringan Komputer”
- Codecademy. (2025). “OSI Model: Complete Guide to the 7 Network Layers”
- AWS. (2026). “What Is the OSI Model? - 7 OSI Layers Explained”
- Checkpoint. (2025). “What is the OSI Model? Understanding the 7 Layers”
- GeeksforGeeks. (2017-2026). “Computer Networks - OSI Model dan TCP/IP Model”

---

**Modul ini disiapkan untuk siswa Teknologi Informasi berusia 15-18 tahun dengan fokus pada pemahaman konsep yang mudah, relevan, dan praktis.**

**Semoga bermanfaat! 🚀**

