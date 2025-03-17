# Virda Septina Putri

3124500058 / D3 IT B

## Tugas 3 OS

### 1. Buatlah flowchart atau diagram proses booting linux

**Jawab:**

!

### 2. Apa perbedaan multiprogramming dengan multitasking?

**Jawab:**

#### a. Multiprogramming

- Digunakan untuk meningkatkan efisiensi sistem.
- Beberapa program yang dimuat di memori dan CPU akan mengeksekusi satu program, lalu berpindah ke program lain saat ada proses yang harus menunggu (misalnya I/O).
- Biasanya digunakan pada sistem batch.
- Tujuannya untuk mengoptimalkan penggunaan CPU.

#### b. Multitasking

- Merupakan perkembangan dari multiprogramming.
- CPU berpindah dari satu proses ke proses lain dengan sangat cepat, sehingga pengguna merasa semua program berjalan bersamaan.
- Memberikan pengalaman interaktif pada pengguna.
- Digunakan pada sistem interaktif seperti desktop OS.

### 3. Apa saja fungsi dari operating system?

**Jawab:**

1. **Manajemen Proses (Process Management)**, yaitu membuat, menghapus, menjeda, menyambung, dan menjadwalkan proses.
2. **Manajemen Memori (Memory Management)**, yaitu melacak penggunaan memori, mengalokasi dan dealokasi memori.
3. **Manajemen Sistem (File System Management)**, yaitu mengelola file dan direktori, akses, serta penyimpanan file.
4. **Manajemen Penyimpanan Massal (Mass-Storage Management)**, yaitu mengelola media penyimpanan seperti HDD, SSD, dan partisi.
5. **Manajemen I/O (Input/Output Subsystem)**, yaitu menyediakan antarmuka ke perangkat keras dan menyembunyikan kompleksitas perangkat dari pengguna.
6. **Proteksi dan Keamanan (Protection and Security)**, yaitu melindungi data dan sistem dari akses tidak sah serta serangan.
7. **Virtualisasi**, yaitu menjalankan OS tamu dalam satu host OS.
8. **Alokasi Sumber Daya (Resource Allocation)**, yaitu mengalokasikan CPU, memori, perangkat I/O, dan yang lain secara efisien.
9. **Interface Pengguna (User Interface)**, yaitu menyediakan CLI atau GUI.

### 4. Apa perbedaan virtualisasi dengan container?

**Jawab:**

| **Virtualisasi**                  | **Container**                     |
|-----------------------------------|-----------------------------------|
| - Menjalankan satu atau lebih sistem operasi (guest OS) di atas OS utama (host OS). | - Menjalankan aplikasi dalam lingkungan terisolasi di dalam satu OS kernel yang sama. |
| - Menggunakan Virtual Machine Manager (VMM) atau hypervisor seperti VMware, VirtualBox. | - Menggunakan tools seperti docker. |
| - Setiap guest OS berjalan dengan kernel-nya sendiri. | - Cocok untuk deploy cepat dan efisien di cloud. |
| - Lebih berat, karena memerlukan satu OS lengkap untuk setiap mesin virtual. | - Lebih ringan dari virtualisasi karena tidak perlu OS lengkap. |
