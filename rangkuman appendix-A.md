# Virda Septina Putri  
3124500058 / D3 IT B  

## APPENDIX  

Tinjauan komprehensif tentang evolusi sistem operasi (OS), menelusuri bagaimana konsep-konsep kunci yang awalnya dikembangkan untuk sistem besar (seperti mainframe dan minikomputer) akhirnya diadopsi oleh sistem yang lebih kecil (seperti PC dan perangkat genggam).  

### 1. Migrasi Fitur  
Sistem operasi modern adalah hasil dari puluhan tahun inovasi yang dimulai dari sistem sederhana hingga kompleks. Fitur seperti virtual memory, multiprogramming, dan GUI awalnya dikembangkan untuk mainframe, tetapi sekarang menjadi standar di perangkat kecil.  

### 2. Era Awal Komputer Manual ke Sistem Batch  

#### 2.1 Komputer Generasi Awal (1940-1950an)  
- **Manchester Mark 1 (1949) dan Ferranti Mark 1 (1951)**:  
  Dioperasikan secara manual melalui console. Programmer memuat instruksi satu per satu menggunakan punched cards atau paper tape. Tidak ada OS; eksekusi program bersifat interaktif dan membutuhkan intervensi manusia secara konstan.  

#### 2.2 Sistem Dedikasi dan Batch  
Masalah utama pada waktu setup yang lama (misal: mounting tape) menyebabkan CPU idle. Solusi bisa didapatkan dengan:  
- **Resident Monitor**: Program kecil yang selalu berada di memori, mengotomatiskan urutan eksekusi job menggunakan control cards (misal: `$JOB`, `$FTN`, `$END`).  
- **Spooling**: Menggunakan disk sebagai buffer untuk input/output, memungkinkan overlap antara komputasi dan I/O. Contoh: Sistem membaca input dari disk sementara CPU menjalankan job lain.  

#### 2.3 Overlapped I/O dan Dampaknya  
Adanya keterbatasan tape sequential, tape harus diisi sepenuhnya sebelum diproses, menyebabkan delay. Revolusi Disk Random-Access yang menyebabkan disk memungkinkan akses cepat ke data di lokasi mana pun, mempercepat spooling dan memunculkan konsep multiprogramming.  

### 3. Sistem Operasi Penting dan Inovasinya  

#### 3.1 Atlas (1950–1960-an): Pelopor Virtual Memory  
- Pertama kali menggunakan core memory sebagai cache untuk drum memory.  
- Algoritma Page-Replacement memprediksi akses memori berdasarkan pola loop, mengganti halaman yang tidak digunakan dalam waktu lama.  
- Konsep ini menjadi dasar virtual memory di OS modern seperti Windows dan Linux.  

#### 3.2 XDS-940 (1960-an): Time-Sharing dan Proses Hierarkis  
- Time-Sharing mendukung banyak pengguna secara interaktif.  
- Proses dinamis memungkinkan pembuatan subproses dan shared memory untuk komunikasi.  
- Privilege separation memisahkan mode user dan kernel untuk keamanan.  

#### 3.3 THE (1965): Desain Berlapis dan Semaphore  
- Layered design membagi OS menjadi lapisan-lapisan terpisah (misal: lapisan hardware, manajemen memori, aplikasi).  
- Semaphore memperkenalkan konsep sinkronisasi proses untuk menghindari race condition.  
- Banker’s Algorithm menjadi solusi pertama untuk deadlock avoidance.  

#### 3.4 RC 4000 (1960-an): Komunikasi via Pesan  
- Microkernel hanya menyediakan fungsi dasar seperti penjadwalan dan komunikasi.  
- Message-Passing merupakan proses berkomunikasi dengan mengirim pesan fixed-size (8 words), konsep yang dipakai di sistem modern seperti Mach.  

#### 3.5 CTSS (1961) dan MULTICS (1965–1970): Time-Sharing Utility  
- **CTSS**:  
  - Multilevel Feedback Queue merupakan Proses dengan CPU burst pendek diprioritaskan.  
  - Dampaknya membuktikan time-sharing layak dipakai, memicu pengembangan MULTICS.  
- **MULTICS**:  
  - Segmented-Paged Memory merupakan gabungan segmentasi dan paging untuk fleksibilitas.  
  - Hierarchical File System adalah struktur direktori mirip UNIX.  
  - Kegagalan Komersial bisa terlalu kompleks, tetapi ide-idenya hidup di UNIX.  

#### 3.6 IBM OS/360 (1960-an): Kesalahan Desain yang Berharga  
- Satu OS untuk seluruh IBM/360.  
- Masalahnya terdapat pada JCL yang rumit karena Job Control Language sulit dipahami.  
- Manajemen memori statis tidak mendukung relokasi dinamis.  
- Kompleksitas berlebihan bisa berakibat fatal.  

#### 3.7 CP/M hingga Windows: Revolusi Personal Computing  
- **CP/M (1970-an)**: OS standar untuk PC 8-bit (Intel 8080).  
- **MS-DOS (1981)**:  
  - Dibuat untuk IBM PC (8086), terinspirasi CP/M tetapi dengan fitur lebih.  
  - Keterbatasan: Tidak ada protected memory atau multitasking.  
- **Mac OS vs. Windows**:  
  - Mac OS (1984): Pertama dengan GUI berbasis mouse.  
  - Windows: Menang karena kompatibilitas hardware yang luas.  

#### 3.8 Mach (1980-an): Microkernel dan Warisan di macOS  
- Kernel minimalis yang mendukung multiprocessing dan emulasi OS lain.  
- **Fitur Unggulan**:  
  - Message-Passing: Komunikasi antar-proses via pesan.  
  - Portability: Berjalan di berbagai arsitektur (VAX, Intel, dll.).  
- Sebagai pewaris Kernel XNU di macOS/iOS menggabungkan Mach dengan komponen BSD.  

#### 3.9 Sistem Capability-Based: Hydra vs. CAP  
- **Hydra**:  
  - Hak akses bisa didefinisikan pengguna.  
  - Prosedur "terpercaya" bisa mendapatkan akses sementara ke objek.  
- **CAP**:  
  - Data merupakan hak akses data.  
  - Software Capability merupakan hak yang diinterpretasikan oleh prosedur.  
  - Keamanan bisa dicapai tanpa kernel kompleks.  

### 4. Kesimpulan  
#### 4.1 Migrasi Fitur  
Inovasi seperti virtual memory (Atlas), time-sharing (CTSS), dan GUI (Mac OS) awalnya eksklusif untuk sistem besar, tetapi sekarang ada di perangkat kecil.  

#### 4.2 Desain vs. Kompleksitas  
Sistem seperti MULTICS dan OS/360 gagal karena terlalu kompleks, sementara UNIX sukses karena kesederhanaannya.  

#### 4.3 Relevansi Modern  
1. Konsep Mach hidup di macOS/iOS.  
2. Spooling berevolusi menjadi sistem cloud printing.  
3. Capability-based security dipakai di sistem seperti seL4 microkernel.  

OS tidak hanya tentang teknologi, tetapi juga tentang pola desain yang berhasil (atau gagal) dan pelajaran yang masih relevan untuk pengembangan OS masa depan.  
