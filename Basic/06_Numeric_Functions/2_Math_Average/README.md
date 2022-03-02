# Average

> Average merupakan fungsi agregat untuk menghitung rata-rata suatu kolom numeric yang dikembalikan dari query dieksekusi.

`AVERAGE` akan menghitung penjumlahan data dan jumlah data sehingga dari suatu kolom numeric dan menghasilkan hasil rata-rata.

## Sintak

```sql
SELECT AVG(nama_kolom) FROM nama_tabel
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

### Menghitung rata-rata data di satu tabel

```sql
SELECT AVG(nilai) as rata_rata FROM tabel_siswa
```
| rata_rata |
|-------------|
| 84          |

### Menghitung rata-rata data dengan kondisi

```sql
SELECT AVG(nilai) as rata_rata FROM tabel_siswa
WHERE asal = 'Indonesia'
```
| rata_rata |
|-------------|
| 80          |

Query diatas hanya menghitung rata-rata dari kolom `nilai` dengan kondisi dikolom `asal` berisi `Indonesia`