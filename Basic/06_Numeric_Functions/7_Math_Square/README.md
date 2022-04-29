# Square

> Square merupakan fungsi untuk mengkuadratkan kolom bertipe number yang dimasukkan.

## Sintak

```sql
SELECT SQUARE(kolom_angka) 
FROM nama_tabel
```

Hasil yang dari fungsi `SQUARE` bertipe data `DESIMAL`


## Query

```sql
SELECT SQUARE(3);
-- Hasil: 9.0
-- kuadrat 3 adalah 9, karena hasil yang dikeluarkan adalah desimal, maka hasil nya 9.0

SELECT SQUARE(3.5);
-- Hasil: 12.25 
```

### Detail Teknis

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server 2008 (diatas)                   | :heavy_check_mark: |
| Azure SQL Database                        | :heavy_check_mark: |
| . .         
