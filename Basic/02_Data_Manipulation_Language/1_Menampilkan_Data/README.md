# SQL SELECT

Query `SELECT` digunakan untuk mengambil semua data yang sudah ada dari database yang kita miliki.<br>
Untuk mengambil data dari database kita perlu mengetahui **nama tabel** dan **nama kolom** yang ingin di ambil

```sql
SELECT nama_kolom, nama_kolom2
FROM nama_tabel
```

## Persiapan

Contoh tabel yang ada di _Materi 2_Menginputkan_Data_

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

## QUERY SELECT

Kita sudah memiliki tabel `SISWA` yang memiliki kolom `nish` dan `nama`
untuk mengambil semua data di tabel bisa menggunakan query :

```sql
SELECT nish, nama
FROM siswa
```

output:
| nish | nama |
| ---- | -------- |
| 1 | Budi |
| 3 | Ani |
| 4 | Poseidon |
| 5 | Hades |

### Penggunaan Asterisk

**Asterisk** `"*"` adalah query yang digunakan untuk mempersingkat dalam pemanggilan semua kolom yang ada dalam sebuah tabel.

```sql
SELECT *
FROM siswa
```

Output:
| nish | nama |
| ---- | -------- |
| 1 | Budi |
| 3 | Ani |
| 4 | Poseidon |
| 5 | Hades |

_nb. penggunaan asterisk seperti diatas tidak berlaku untuk semua jenis DBMS, tedapat DBMS yang tidak mempunyai fitur ini_

### Mengambil Data Dibeberapa Kolom

Untuk mengambil beberapa kolom yang ada di tabel, hal yang dilakukan adalah hanya menuliskan nama kolom yang ingin diambil :

```sql
SELECT nama
FROM siswa
```

output:
| nama |
| -------- |
| Budi |
| Ani |
| Poseidon |
| Hades |

[<< Materi sebelumnya](https://github.com/bellshade/SQL/tree/main/Basic/01_Pengenalan/4_SQL_Comment) | [Materi selanjutnya >>](https://github.com/bellshade/SQL/tree/main/Basic/02_Data_Manipulation_Language/2_Menginput_Data)