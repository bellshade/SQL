# SQRT

> SQRT merupakan fungsi untuk menghitung akar kuadrat suatu nilai numeric.

`SQRT` menghitung akar kuadra suatu nilai numeric dari tiap data yang di kembalikan suatu query

## Sintak

```sql
SELECT SQRT(nama_kolom) FROM nama_tabel
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
  ("Veronica Boyle","Kolombia",81),
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
| 4  | Veronica Boyle  | Kolombia  |81|
| 5  | Emmanuel Wells  | Indonesia   |90|
| 6  | Sacha Henry     | Indonesia |80|
| 7  | Gavin Caldwell  | Indonesia  |70|
| 8  | Carson Chandler | Singapura |90|
| 9  | Albert Kylynn   | Prancis  |80|
| 10 | Tamara Wyatt    | Prancis  |90|

### Menghitung akar kuadrat satu kolom

```sql
SELECT SQRT(nilai) as hasil_akar_kuadrat FROM tabel_siswa
```
| hasil_akar_kuadrat |
|--------------------|
| 9.4868329805051381 |
| 8.3666002653407556 |
| 9.4868329805051381 |
| 9.0                |
| 9.4868329805051381 |
| 8.9442719099991592 |
| 8.3666002653407556 |
| 9.4868329805051381 |
| 8.9442719099991592 |
| 8.9442719099991592 |

Query diatas menghitung akar kuadrat dari kolom `nilai` dari setiap baris data yang ada di tabel `tabel_siswa`

### Menghitung akar kuadrat satu data

```sql
SELECT SQRT(nilai) as hasil_akar_kuadrat FROM tabel_siswa
WHERE asal = 'Kolombia'
```
| hasil_akar_kuadrat |
|-------------|
| 9.0          |

Query diatas menghitung akar kuadrat dari kolom `nilai` dengan kondisi kolom `asal` memiliki nilai *Kolombia* 