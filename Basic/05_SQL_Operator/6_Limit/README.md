# LIMIT

> LIMIT merupakan perintah untuk menentukan jumlah data yang akan diberikan.

**LIMIT** digunakan pada tabel yang memiliki ribuan atau lebih data karena saat memberikan data yang berjumlah besar, kinerja dari database akan ikut terpengaruhi.

## Query

_Note_ : setiap database memiliki cara untuk menggunakan LIMIT.

### MYSQL

```sql
SELECT * FROM nama_tabel LIMIT 20;
```

Query diatas akan mengeluarkan 20 data saat dieksekusi.

### SQL SERVER 2012

Pada _SQL Server_ penggunaan _LIMIT_ bisa menggunakan `TOP`.

```sql
SELECT TOP 10 * FROM nama_tabel;
```

Query diatas akan mengeluarkan 10 data teratas saat dieksekusi.

### MARIA DB

Pada _Maria DB_ bisa menggunakan _LIMIT_.

```sql
SELECT * FROM nama_tabel LIMIT 15;
```

Query diatas akan mengeluarkan 15 data teratas saat dieksekusi.

### Oracle 12

Pada _SQL Server_ penggunaan _LIMIT_ bisa menggunakan `FETCH FIRST number ROWS ONLY`.

```sql
SELECT nama_kolom
FROM nama_tabel
FETCH FIRST 44 ROWS ONLY;
```

Query diatas akan mengeluarkan 44 data teratas saat dieksekusi.

[<< Materi sebelumnya](https://github.com/bellshade/SQL/tree/main/Basic/05_SQL_Operator/5_Aliasing) | [Materi selanjutnya >>](https://github.com/bellshade/SQL/tree/main/Basic/05_SQL_Operator/7_OrderBy)