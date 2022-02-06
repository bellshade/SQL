# MAX dan MIN

> MAX merupakan fungsi agregat untuk mencari nilai TERBESAR dari suatu kolom yang dikembalikan dari query yang dieksekusi.

> MIN merupakan fungsi agregat untuk mencari nilai TERKECIL dari suatu kolom yang dikembalikan dari query yang dieksekusi.

`COUNT` menghitung jumlah baris data query `SELECT` yang dieksekusi.

## Sintak

```sql
SELECT MAX(nama_kolom) FROM nama_tabel
```

```sql
SELECT MIN(nama_kolom) FROM nama_tabel
```

## Query

Contoh query insert untuk data dummy.

```sql
DROP TABLE IF EXISTS tabel_siswa;

CREATE TABLE tabel_siswa (
  id mediumint(8) unsigned NOT NULL auto_increment,
  nama varchar(255) default NULL,
  asal varchar(100) default NULL,
  nilai int,
  PRIMARY KEY (id)
) AUTO_INCREMENT=1;

INSERT INTO tabel_siswa (nama,asal)
VALUES
  ("Iliana Davidson","Polandia",90),
  ("Jesse Chandler","Polandia",80),
  ("Lester Trujillo","Polandia",90),
  ("Veronica Boyle","Kolombia",90),
  ("Emmanuel Wells","Indonesia",100),
  ("Sacha Henry","Indonesia",80),
  ("Gavin Caldwell","Indonesia",70),
  ("Carson Chandler","Singapura",90),
  ("Albert Kylynn","Prancis",80),
  ("Tamara Wyatt","Prancis",90);

SELECT * FROM tabel_siswa
```

| id | nama            | asal      | nilai|
|----|-----------------|-----------|-----------|
| 1  | Iliana Davidson | Polandia  |90|
| 2  | Jesse Chandler  | Polandia  |80|
| 3  | Lester Trujillo | Polandia  |90|
| 4  | Veronica Boyle  | Kolombia  |90|
| 5  | Emmanuel Wells  | Indonesia   |100|
| 6  | Sacha Henry     | Indonesia |80|
| 7  | Gavin Caldwell  | Indonesia  |70|
| 8  | Carson Chandler | Singapura |90|
| 9  | Albert Kylynn   | Prancis  |80|
| 10 | Tamara Wyatt    | Prancis  |90|

### Mencari nilai terbesar data di satu tabel

```sql
SELECT MAX(nilai) as nilai_terbesar FROM tabel_siswa
```
| nilai_terbesar |
|-------------|
| 100          |

### Mencari nilai terbesar data dengan kondisi

```sql
SELECT MAX(nilai) as nilai_terbesar FROM tabel_siswa
WHERE asal = 'Polandia'
```
| nilai_terbesar |
|-------------|
| 90          |

Query diatas hanya mencari nilai terbesar dari kolom `nilai` dengan kondisi dikolom `asal` berisi `Polandia`


### Mencari nilai terkecil data di satu tabel

```sql
SELECT MIN(nilai) as nilai_terkecil FROM tabel_siswa
```
| nilai_terkecil |
|-------------|
| 70          |

### Mencari nilai terkecil data dengan kondisi

```sql
SELECT MIN(nilai) as nilai_terkecil FROM tabel_siswa
WHERE asal = 'Polandia'
```
| nilai_terkecil |
|-------------|
| 80          |

Query diatas hanya mencari nilai terkecil dari kolom `nilai` dengan kondisi dikolom `asal` berisi `Polandia`