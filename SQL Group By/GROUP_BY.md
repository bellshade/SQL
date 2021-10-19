# GROUP BY

**GROUP BY** adalah salah satu perintah yang digunakan di SQL untuk **mengelompokkan data** berdasarkan kolom yang dipilih, biasanya untuk mendapat suatu hasil dari perhitungan `rata-rata | AVG()`, `penjumlahan | SUM()`, `nilai tertinggi | MAX()`, `nilai terkecil | MIN()` dan `jumlah baris data | COUNT()`

Kita akan menggunakan contoh data ini

tabel **Penjualan**

| Id  | Nama  | Barang | Jumlah |
| --- | ----- | ------ | ------ |
| 1   | Joni  | Sabun  | 2      |
| 2   | Tera  | Teh    | 4      |
| 3   | Andra | Sabun  | 3      |
| 4   | Joni  | Sapu   | 1      |
| 5   | Tera  | Gelas  | 2      |
| 6   | Joni  | Mie    | 2      |
| 7   | Joni  | Sabun  | 3      |

berikut query untuk membuat dan _insert_ tabel **Penjualan**

```sql
CREATE TABLE Penjualan{
    Id int,
    Nama varchar(50),
    Barang varchar(50),
    Jumlah int,
}

INSERT INTO Penjualan VALUES (1,'Joni','Sabun',2)
INSERT INTO Penjualan VALUES (1,'Tera','teh',4)
INSERT INTO Penjualan VALUES (1,'Andra','Sabun',3)
INSERT INTO Penjualan VALUES (1,'Joni','Sapu',1)
INSERT INTO Penjualan VALUES (1,'Tera','Gelas',2)
INSERT INTO Penjualan VALUES (1,'Joni','Mie',2)
```

## GROUP BY Query

### Sintaks

```sql
SELECT nama_kolom,nama_kedua
FROM nama_tabel
GROUP BY nama_kolom,nama_kedua
```

Dalam penggunaan **GROUP BY**, hanya kolom yang akan menjadi dasar dari pengelompokan data yang bisa ditampilkan (SELECT).

Contoh - kita ingin mengelompokkan data berdasar kolom `Nama`

```sql
SELECT Nama
FROM Penjulaan
GROUP BY Nama
```

output :

| Nama  |
| ----- |
| Joni  |
| Tera  |
| Andra |

Jika kita ingin menampilkan kolom `Barang` juga (`SELECT Nama, Barang`) maka di `GROUP BY` harus ditambahkan kolom `Barang` juga (`GROUP BY Nama, Barang`), jika tidak akan terjadi _error_

## MenggunakanCOUNT, MAX, MIN, SUM dan AVG

### `Count()`

_Count()_ adalah query untuk mendapat **jumlah baris dari suatu table**, tetapi karena kita menggunakan GROUP BY sehingga hasil nya adalah **jumlah baris dari suatu data**

Contoh - Mencari jumlah barang yang dibeli dari tiap `Nama`

```sql
SELECT Nama, count(barang) as jumlah_barang
FROM Penjulaan
GROUP BY Nama
```

output
| Nama | jumlah_Barang |
|-------|---------------|
| Joni | 4 |
| Tera | 2 |
| Andra | 1 |

karena _Joni_ membeli 4 barang (Sabun 2x, sapu dan mie) maka akan keluar 4 di kolom hitung barang

### `Sum()`

_Sum()_ adalah query untuk mendapat **Penjumlahan data dari 1 kolom yang dipilih**, tetapi karena kita menggunakan GROUP BY sehingga hasil nya adalah **Penjumlahan data dari 1 kolom dipilih berdasarkan pengelompokan data**

Contoh - Jumlahkan total barang yang dibeli berdasarkan`Nama`

```sql
SELECT Nama, sum(jumlah) as jumlah_barang
FROM Penjulaan
GROUP BY Nama
```

output
| Nama | jumlah_barang |
|-------|---------------|
| Joni | 8 |
| Tera | 6 |
| Andra | 3 |

Joni membeli _Sabun 2x (5)_, _sapu (1)_ dan _mie (2)_ maka hasil nya **8**

### `AVG()`

_AVG()_ adalah query untuk mendapat **rata-rata dari 1 kolom yang dipilih**, tetapi karena kita menggunakan GROUP BY sehingga hasil nya adalah **rata-rata dari 1 kolom yang dipilih berdasarkan pengelompokan data**

Contoh - rata-rata barang yang dibeli berdasarkan`Nama`

```sql
SELECT Nama, avg(barang) as rata_rata
FROM Penjulaan
GROUP BY Nama
```

| Nama  | rata_rata |
| ----- | --------- |
| Joni  | 2         |
| Tera  | 2         |
| Andra | 3         |

Karena Joni membeli 4 barang (_count()_) dengan jumlah 8 (_sum()_) maka `8/4 = 2`

### `MIN() dan MAX()`

_MIN()_ dan _MAX()_ menggunakan GROUP BY sehingga hasil nya adalah **nilai minimal dan maksimal berdasarkan pengelompokan data**

Contoh - minimal dan maksimal barang yang dibeli berdasarkan`Nama`

```sql
SELECT Nama, min(jumlah) as minimal, max(jumlah) as maksimal,
FROM Penjulaan
GROUP BY Nama
```

| Nama  | minimal | maksimal |
| ----- | ------- | -------- |
| Joni  | 1       | 3        |
| Tera  | 2       | 4        |
| Andra | 3       | 3        |

## Menggunakan 2 Kolom

_GROUP BY_ juga dapat digunakan untuk mengelompokan data berdasarkan 2 Kolom

```sql
SELECT Nama, Barang, sum(Jumlah) as jumlah_barang
FROM Penjulaan
GROUP BY Nama,Barang
```

output :

| Nama  | Barang | Jumlah |
| ----- | ------ | ------ |
| Joni  | Sabun  | 5      |
| Tera  | Teh    | 4      |
| Andra | Sabun  | 3      |
| Joni  | Sapu   | 1      |
| Tera  | Gelas  | 2      |
| Joni  | Mie    | 2      |

Pada `Nama = Joni` dan `Barang = Sabun`, karna ada 2 baris data yang memiliki nilai yang sama maka kolom jumlah pada baris tersebut akan dijumlahkan `2 + 3 = 5`

## Menggunakan 2 Tabel

`GROUP BY` juga dapat mengelompokan data dari 2 tabel yang berbeda, gabungkan query `JOIN` dengan query `GROUP BY`, dan ikuti aturan pengggunaan `GROUP BY`.

```sql
SELECT  nama_tabel_1.nama_kolom_tabel_1,
        nama_tabel_2.nama_kolom_tabel_2,
        sum(nama_tabel_2.nama_kolom_jumlah)
FROM nama_tabel_1
JOIN nama_tabel_2
ON nama_tabel_2.id = nama_tabel_1.tabel2_id
GROUP BY nama_tabel_1.nama_kolom,
        nama_tabel_2.nama_kolom
```

Contoh diatas adalah penggabungan tabel `nama_tabel_1` dan tabel `nama_tabel_2`.

Kolom yang ditampilkan adalah kolom `nama_kolom_tabel_1` dan `nama_kolom_tabel_2` dan *method* `sum` pada kolom `nama_kolom_jumlah`

### Compatibility Query

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server                     | :heavy_check_mark: |
| MariaDB                        | :heavy_check_mark: |
| . .                            |                    |
