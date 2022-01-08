# SQL DELETE

Query `DELETE` di SQL digunakan untuk menghapus data yang sudah ada di sebuah table dari database yang kita miliki.<br>

### DELETE sintak

```sql
DELETE FROM nama_tabel
WHERE kondisi --optional
```

### Contoh Penggunaan

#### Persiapkan

_Materi 2_Menginputkan_Data_

```sql
-- Membuat Database Sekolah
CREATE DATABASE sekolah;

-- Memakai Database Sekolah
USE sekolah;

-- Membuat tabel siswa yang terdiri dari nisn dan nama
CREATE TABLE siswa (
  nisn int NOT NULL, -- int adalah bilangan bulat -> Integer
  nama varchar(50), -- varchar adalah karakter, 50 adalah limit maksimal panjang karakter
  primary key(nisn) -- primary key adalah unique value dari data tersebut, disini kita membuat primary key nya adalah nisn (nomor induk siswa nasional), saat membuat primary key tambahkan NOT NULL agar mempertegas kolom nisn tidak boleh kosong saat memasukan data
  );

-- Memasukkan data siswa baru ke dalam seluruh kolom dari tabel siswa (nidn dan nama)
INSERT INTO siswa VALUES(1,"Budi");

-- Memasukkan multiple data ke dalam tabel siswa
INSERT INTO siswa VALUES(3,"Ani"), (4,"Poseidon"), (5,"Hades");
```

`SELECT * FROM SISWA` --> referensi tabel **2-Menginput-Data**

| nish | nama     |
| ---- | -------- |
| 1    | Budi     |
| 3    | Ani      |
| 4    | Poseidon |
| 5    | Hades    |

### Delete data secara spesifik

- Menghapus kolom **nama** `Budi`

```SQL
-- cara 1
DELETE FROM SISWA
WHERE nama = 'Budi' -- Menggunakan kondisi di kolom `nama`

-- cara 2
DELETE FROM SISWA
WHERE nish = 1 -- Menggunakan kondisi di kolom `nish`
```

| nish | nama     |
| ---- | -------- |
| 3    | Ani      |
| 4    | Poseidon |
| 5    | Hades    |

### Delete semua data di suatu tabel

- Menghapus semua data dalam 1 tabel

```SQL
DELETE FROM SISWA
```

Hasil :
| nish | nama |
|------|----------|
| | |

---

### Compatibility Query

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server                     | :heavy_check_mark: |
| MariaDB                        | :heavy_check_mark: |
| . .                            |                    |
