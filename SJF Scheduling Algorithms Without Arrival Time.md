# SJF

## LAPORAN SISTEM OPERASI  
### TUGAS CODING UNTUK SJF DAN SRTF  

**Disusun oleh:**  
- Fandra Salsabilla Oktorasari (3124500040)  
- Wina Rahmalia (3124500052)  
- Virda Septina Putri (3124500058)  

**Dosen Pengajar:** Dr Ferry Astika Saputra ST, M.Sc  

**PROGRAM STUDI D3 TEKNIK INFORMATIKA**  
**POLITEKNIK ELEKTRONIKA NEGERI SURABAYA (PENS)**  
**TAHUN 2025**

---

## SJF Scheduling Without Arrival Time

### Penjelasan:
- **Non-Preemptive** → setelah suatu proses memulai dieksekusi maka tidak akan dihentikan hingga selesai.  
- Karena tidak ada waktu kedatangan, semua proses dianggap tiba secara bersamaan.

### Langkah-langkah:
1. P4 (BT=1) → Paling kecil → jalan pertama kali.  
2. P2 (BT=3) dan P5(BT=3) → tie (sama besar), urutan bisa berdasarkan input (P2 terlebih dahulu).  
3. P5 (BT=3)  
4. P3 (BT=4)  
5. P1 (BT=7) → paling terakhir.

- **Completion Time (CT):** Waktu saat proses selesai dieksekusi.
- **Turnaround Time:** (1+4+7+11+18)/5 = 8.2  
- **Waiting Time:** (0+1+4+7+11)/5 = 4.6  

**Kesimpulan:**  
Algoritma SJF Non-Preemptive menghasilkan waktu tunggu dan turnaround time yang optimal jika arrival time tidak dipertimbangkan. Namun, jika banyak proses kecil datang terlambat, bisa menyebabkan *starvation* untuk proses dengan burst time besar.

---

## SJF Scheduling Algorithms With Arrival Time

### Penjelasan dan Perhitungan:

1. **P3 (AT=0, BT=3)**  
   - CT = 3  
   - TAT = 3 - 0 = 3  
   - WT = 0  

2. **Waktu = 3**  
   - P1 (AT=2, BT=5), P2 (AT=1, BT=6)  
   - Pilih P1 (BT=5)  
   - CT = 8  
   - TAT = 8 - 2 = 6  
   - WT = 6 - 5 = 1  

3. **Waktu = 8**  
   - P2 (AT=1), P4 (AT=5), P5 (AT=8)  
   - Pilih P4 (BT=4)  
   - CT = 12  
   - TAT = 12 - 5 = 7  
   - WT = 7 - 4 = 3  

4. **Waktu = 12**  
   - Pilih P2 (BT=6)  
   - CT = 18  
   - TAT = 18 - 1 = 17  
   - WT = 17 - 6 = 11  

5. **Waktu = 18**  
   - Pilih P5 (BT=7)  
   - CT = 25  
   - TAT = 25 - 8 = 17  
   - WT = 17 - 7 = 10  

---

## SRTF Scheduling Algorithms

### 1. Data Awal

| Proses | Arrival Time (AT) | Burst Time (BT) |
|--------|-------------------|-----------------|
| P1     | 0                 | 6               |
| P2     | 2                 | 3               |
| P3     | 6                 | 9               |
| P4     | 4                 | 1               |
| P5     | 8                 | 2               |

### 2. Timeline Eksekusi

| Waktu | Proses Berjalan | Keterangan |
|-------|------------------|------------|
| 0     | P1              | Hanya P1 yang hadir |
| 1     | P1              | Sisa 5 |
| 2     | P2              | Preempt P1 |
| 3     | P2              | Sisa 2 |
| 4     | P2              | P4 datang (sama) |
| 5     | P2 selesai → P4 | P4 lebih pendek |
| 6     | P1              | P1 kembali |
| 7–10  | P1              | Selesaikan P1 |
| 10–12 | P5              | BT=2 |
| 12–21 | P3              | Satu-satunya tersisa |

### 3. Diagram Gantt


# SJF Scheduling Without Arrival Time

![Output (Without Arrival Time ](https://github.com/virdasp14/SisOp-2025/blob/main/Output%20(Without%20Arrival%20Time)%20SJF%20Scheduling%20Algorithms.jpeg?raw=true)

![Tabel Eksekusi](https://github.com/virdasp14/SisOp-2025/blob/main/Tabel%20Eksekusi%20(Without%20Arrival%20Time)%20SJF%20Scheduling%20Algorithm.jpeg?raw=true)



## Penjelasan

- **Non-Preemptive**: Setelah suatu proses mulai dieksekusi, maka proses tersebut tidak akan dihentikan hingga selesai.
- Karena **tidak ada waktu kedatangan** (arrival time), maka semua proses dianggap tiba **secara bersamaan**.

## Langkah-langkah Penjadwalan

1. P4 (BT = 1) → Paling kecil → dijalankan pertama kali.
2. P2 (BT = 3) dan P5 (BT = 3) → tie (sama besar), maka urutan berdasarkan input (P2 terlebih dahulu).
3. P5 (BT = 3)
4. P3 (BT = 4)
5. P1 (BT = 7) → Paling akhir.

## Rata-rata

- **Turnaround Time (TAT)** = (1 + 4 + 7 + 11 + 18) / 5 = **8.2**
- **Waiting Time (WT)** = (0 + 1 + 4 + 7 + 11) / 5 = **4.6**

## Kesimpulan

Algoritma **SJF Non-Preemptive** menghasilkan **waktu tunggu dan turnaround time yang optimal** jika **arrival time tidak dipertimbangkan**. Namun, jika banyak proses kecil datang terlambat, maka harus menunggu, sehingga SJF dapat menyebabkan **starvation** untuk proses dengan burst time besar.
