# SQL UPDATE

Bahasa Query dari `UPDATE` digunakan untuk mengubah data yang sudah ada di sebuah table dari database yang kita miliki.

### UPDATE sintak

```sql
UPDATE nama_tabel
SET nama_kolom = nilai_baru, nama_kolom_2 = nilai_baru_2
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

### Update semua data di satu kolom

- Ubah semua yang ada di kolom **nama** menjadi `Bob`

```SQL
UPDATE SISWA
SET nama = 'Bob'
```

Hasil :
| nish | nama |
|------|----------|
| 1 | Bob |
| 3 | Bob |
| 4 | Bob |
| 5 | Bob |

### Update data secara spesifik

- Ubah kolom **nama** `Budi` saja menjadi `Alice`

```SQL
-- cara 1
UPDATE SISWA
SET nama = 'Alice'
WHERE nama = 'Budi' -- Menggunakan kondisi di kolom `nama`

-- cara 2
UPDATE SISWA
SET nama = 'Alice'
WHERE nish = 1 -- Menggunakan kondisi di kolom `nish`
```

Hasil :
| nish | nama |
|------|----------|
| 1 | Alice |
| 3 | Ani |
| 4 | Poseidon |
| 5 | Hades |

### Update 2 data secara spesifik

- Ubah kolom **nama** `Alice` saja menjadi `Vega`
- Ubah kolom **nisn** `1` saja menjadi `10`

```SQL
-- cara 1
UPDATE SISWA
SET nama = 'Vega', nisn = 10
WHERE nama = 'Alice' -- Menggunakan kondisi di kolom `nama`

-- cara 2
UPDATE SISWA
SET nama = 'Vega', nisn = 10
WHERE nish = 1 -- Menggunakan kondisi di kolom `nish`
```

Hasil :
| nish | nama |
|------|----------|
| 10 | Vega |
| 3 | Ani |
| 4 | Poseidon |
| 5 | Hades |

### Compatibility Query

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server                     | :heavy_check_mark: |
| MariaDB                        | :heavy_check_mark: |
| . .                            |                    |

[<< Materi sebelumnya](https://github.com/bellshade/SQL/tree/main/Basic/02_Data_Manipulation_Language/2_Menginput_Data) | [Materi selanjutnya >>](https://github.com/bellshade/SQL/tree/main/Basic/02_Data_Manipulation_Language/4_Menghapus_Data)