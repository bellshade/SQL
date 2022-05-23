# Random

> Random merupakan fungsi yang menghasilkan nilai bilangan rill secara acak dari bilang 0 sampai 1.

## Sintak

```sql
SELECT RAND() as nilai
```

Hasil yang dari fungsi `RAND` bertipe data `FLOAT`

## Query

### Menghasilkan nilai acak

```sql
SELECT RAND() as nilai;
-- Hasil: 0.6580458928064617 | setiap eksekusi query akan menghasilkan nilai yang berbeda
```

### Menyimpan nilai acak

Nilai acak yang dibuat dapat disimpan juga dengan menggunakan *seed* berupa angka.

```sql
SELECT RAND(2);
-- Hasil: 0.6555866465490187 
-- nilai 2 didalam RAND() adalah seed. Setiap mengeksekusi menggunakan seed yang sama (contoh : 2) akan menghasilkan hasil yang sama
```
*nilai seed akan berubah jika server mati*

### Menghasilkan nilai acak diluar 0 dan 1

Jika ingin menghasilkan nilai diliar 0 dan 1, contoh antara nilai 2 hingga 10.

Jika ingin menghasilkan nilai antara 2 hingga 10 biasanya menambahkan operasi matematika.

```sql
SELECT RAND()*(10-2)+2;
-- Hasil: 5.8064617658045892 | setiap eksekusi query akan menghasilkan nilai yang berbeda, >2 dan <10
-- menambahkan operasi matematika untuk menghasilkan nilai yang diinginkan 
```

### Detail Teknis

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server 2008 (diatas)                   | :heavy_check_mark: |
| Azure SQL Database                        | :heavy_check_mark: |
| . .         
