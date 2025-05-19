
# SJF Scheduling Without Arrival Time

## Penjelasan

- **Non-Preemptive**: Setelah suatu proses mulai dieksekusi, maka proses tersebut tidak akan dihentikan hingga selesai.
- Karena **tidak ada waktu kedatangan** (arrival time), maka semua proses dianggap tiba **secara bersamaan**.

## Langkah-langkah Penjadwalan

1. P4 (BT = 1) → Paling kecil → dijalankan pertama kali.
2. P2 (BT = 3) dan P5 (BT = 3) → tie (sama besar), maka urutan berdasarkan input (P2 terlebih dahulu).
3. P5 (BT = 3)
4. P3 (BT = 4)
5. P1 (BT = 7) → Paling akhir.

## Tabel Eksekusi

| Proses | Burst Time (BT) | Completion Time (CT) | Turnaround Time (TAT) | Waiting Time (WT) |
|--------|------------------|----------------------|------------------------|-------------------|
| P4     | 1                | 1                    | 1                      | 0                 |
| P2     | 3                | 4                    | 4                      | 1                 |
| P5     | 3                | 7                    | 7                      | 4                 |
| P3     | 4                | 11                   | 11                     | 7                 |
| P1     | 7                | 18                   | 18                     | 11                |

## Rata-rata

- **Turnaround Time (TAT)** = (1 + 4 + 7 + 11 + 18) / 5 = **8.2**
- **Waiting Time (WT)** = (0 + 1 + 4 + 7 + 11) / 5 = **4.6**

## Kesimpulan

Algoritma **SJF Non-Preemptive** menghasilkan **waktu tunggu dan turnaround time yang optimal** jika **arrival time tidak dipertimbangkan**. Namun, jika banyak proses kecil datang terlambat, maka harus menunggu, sehingga SJF dapat menyebabkan **starvation** untuk proses dengan burst time besar.
