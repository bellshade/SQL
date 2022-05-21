# Floor

> Floor merupakan fungsi untuk membulatkan suatu nilai ke bilangan yang lebih kecil.

biasanya digunakan untuk menghilangkan angka dibelakang koma (`,`) pada bilangan desimal dan membulatkan suatu nilai.

## Sintak

```sql
SELECT FLOOR(kolom_angka) 
FROM nama_tabel
```

Hasil yang dari fungsi `FLOOR` bertipe data `INTEGER`

## Query

```sql
SELECT FLOOR(22.9);
-- Hasil: 22
-- Dibulatkan ke 22, angka dibelakang koma dihilangkan untuk dibulatkan ke angka lebih kecil

SELECT FLOOR(-13.5);
-- Hasil: -14
-- Jika angka negatif maka angka dibelakang koma dihilangkan akan dibulatkan ke angka yang lebih kecil (-14 lebih besar dari -13)
```

### Detail Teknis

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server 2008 (diatas)                   | :heavy_check_mark: |
| Azure SQL Database                        | :heavy_check_mark: |
| . .         
