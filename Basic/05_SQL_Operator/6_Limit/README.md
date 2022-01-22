# LIMIT

> LIMIT merupakan perintah untuk menentukan jumlah data yang akan diberikan.

**LIMIT** biasa nya digunakan bada tabel yang memiliki ribuan atau lebih data karena saat memberikan data yang berjumlah besar, kinerja dari database akan ikut terpengaruhi.

## Query

*Note* : setiap database memiliki cara untuk menggunakan LIMIT

### MYSQL

```sql
SELECT * FROM nama_tabel LIMIT 20;
```
Query diatas akan mengeluarkan 20 data saat dieksekusi

### SQL SERVER 2012

Pada *SQL Server* peggunaan *LIMIT* bisa menggunakan `TOP`.

```sql
SELECT TOP 10 * FROM nama_tabel;
```

Query diatas akan mengeluarkan 10 data teratas saat dieksekusi

### MARIA DB

Pada *Maria DB* bisa menggunakan *LIMIT*.

```sql
SELECT * FROM nama_tabel LIMIT 15;
```

Query diatas akan mengeluarkan 15 data teratas saat dieksekusi

### Oracle 12

Pada *SQL Server* peggunaan *LIMIT* bisa menggunakan `FETCH FIRST number ROWS ONLY`.

```sql
SELECT nama_kolom
FROM nama_tabel
FETCH FIRST 44 ROWS ONLY;
```

Query diatas akan mengeluarkan 44 data teratas saat dieksekusi
