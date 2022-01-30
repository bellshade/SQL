# Count

> COUNT merupakan fungsi agregat untuk menghitung jumlah baris data yang dikembalikan dari query yang dieksekusi.

`COUNT` menghitung jumlah baris data query `SELECT` yang dieksekusi.

## Sintak

```sql
SELECT COUNT(*) FROM nama_tabel
```

```sql
SELECT COUNT(nama_kolom) FROM nama_tabel
```

## Query

Contoh query insert untuk data dummy.

```sql
DROP TABLE IF EXISTS tabel_siswa;

CREATE TABLE tabel_siswa (
  id mediumint(8) unsigned NOT NULL auto_increment,
  nama varchar(255) default NULL,
  asal varchar(100) default NULL,
  PRIMARY KEY (id)
) AUTO_INCREMENT=1;

INSERT INTO tabel_siswa (nama,asal)
VALUES
  ("Iliana Davidson","Polandia"),
  ("Jesse Chandler","Prancis"),
  ("Lester Trujillo","Polandia"),
  ("Veronica Boyle","Kolombia"),
  ("Emmanuel Wells","Nigeria"),
  ("Sacha Henry","Indonesia"),
  ("Gavin Caldwell","Malaysia"),
  ("Carson Chandler","Singapura"),
  ("Albert Kylynn","Prancis"),
  ("Tamara Wyatt","Prancis");

SELECT * FROM tabel_siswa
```

| id | nama            | asal      |
|----|-----------------|-----------|
| 1  | Iliana Davidson | Polandia  |
| 2  | Jesse Chandler  | Prancis  |
| 3  | Lester Trujillo | Polandia  |
| 4  | Veronica Boyle  | Kolombia  |
| 5  | Emmanuel Wells  | Nigeria   |
| 6  | Sacha Henry     | Indonesia |
| 7  | Gavin Caldwell  | Malaysia  |
| 8  | Carson Chandler | Singapura |
| 9  | Albert Kylynn   | Prancis  |
| 10 | Tamara Wyatt    | Prancis  |


### Menghitung data di satu tabel

```sql
SELECT COUNT(*) as jumlah_data FROM tabel_siswa
```
| jumlah_data |
|-------------|
| 10          |

### Menghitung data dengan kondisi

```sql
SELECT COUNT(*) as jumlah_data FROM tabel_siswa
WHERE asal = 'Prancis'
```
| jumlah_data |
|-------------|
| 3          |

Query diatas menampilkan data yang memiliki data `'Prancis'` pada kolom `asal`, yaitu hanya **3** baris data. 
Sehingga hasil dari `COUNT(*)` juga **3**.