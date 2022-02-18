# Sum

> Sum merupakan fungsi agregat untuk menjumlahkan suatu kolom numeric yang dikembalikan dari query dieksekusi.

`Sum` akan menjumlahkan data dari suatu kolom numeric dan menghasilkan hasil penjumlahan semua data

## Sintak

```sql
SELECT SUM(nama_kolom) FROM nama_tabel
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
  ("Jesse Chandler","Polandia",70),
  ("Lester Trujillo","Polandia",90),
  ("Veronica Boyle","Kolombia",90),
  ("Emmanuel Wells","Indonesia",90),
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
| 2  | Jesse Chandler  | Polandia  |70|
| 3  | Lester Trujillo | Polandia  |90|
| 4  | Veronica Boyle  | Kolombia  |90|
| 5  | Emmanuel Wells  | Indonesia   |90|
| 6  | Sacha Henry     | Indonesia |80|
| 7  | Gavin Caldwell  | Indonesia  |70|
| 8  | Carson Chandler | Singapura |90|
| 9  | Albert Kylynn   | Prancis  |80|
| 10 | Tamara Wyatt    | Prancis  |90|

### Menghitung hasil penjumlah kolom nilai

```sql
SELECT SUM(nilai) as hasil_penjumlahan FROM tabel_siswa
```
| hasil_penjumlahan |
|-------------|
| 840          |

### Menghitung hasil penjumlah kolom nilai dengan kondisi

```sql
SELECT SUM(nilai) as hasil_penjumlahan FROM tabel_siswa
WHERE asal = 'Indonesia'
```
| hasil_penjumlahan |
|-------------|
| 240          |

Query diatas hanya menghitung penjumlahan dari kolom `nilai` dengan kondisi dikolom `asal` berisi `Indonesia`