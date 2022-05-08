# Round

> Round merupakan fungsi membulatkan angka DESIMAL yang dikhusukan untuk pembulatan dibelakang koma.

## Sintak

```sql
SELECT ROUND(kolom_desimal, posisi_pembulatan, operation) 
FROM nama_tabel
```

## Parameter

### Kolom_desimal
WAJIB - Kolom yang berisi data desimal dari suatu table yang akan dibulatkan.

Dengan aturan : 
* jika nilai paling kanan `>= 5` maka angka sebelah kiri nya ditambah 1 dan nilai paling kanan menjadi 0.  
* jika nilai paling kanan `< 5` maka angka sebelah kiri nya ditambah tidak berubah dan nilai paling kanan menjadi 0.  

### posisi_pembulatan
* WAJIB 
* Parameter yang menunjukan digit mana yang akan dibulatkan sesuai nilai pada digit yang ada dikanannya. nilai `1` berarti angka pertama sebelah kanan setelah koma

Contoh `125,315`

Jika berisi nilai `1`, maka angka `3` yang akan menjadi nilai pembulatan - `125,300`

Jika berisi nilai `2`, maka angka `1` yang akan menjadi nilai pembulatan - `125,320`

Jika berisi nilai `-1`, maka angka `2` yang akan menjadi nilai pembulatan - `130,000`

### operation
OPTIONAL Nilai defaultnya adalah 0 - Jika berisi 0, nilai Kolom_desimal akan dibulatkan ke angka desimal. Jika nilai lain dari 0, hasilnya akan dipotong menjadi 0 didigit sesuai posis_pembulatan.

## Query

```sql
SELECT ROUND(125.315, 2);
-- Hasil: 125.320 
-- Angka yang dibulat kan adalah 15 menjadi 20

SELECT ROUND(125.315, 2, 0);
-- Hasil: 125.320 
-- Angka yang dibulat kan adalah 15 menjadi 20, dan karena operation secara default bernilai 0

SELECT ROUND(125.315, 0);
-- Hasil: 125.000 
-- Angka yang dibulat kan adalah 5.315 menjadi 5.000,

SELECT ROUND(125.315, -1);
-- Hasil: 130.000 
-- Angka yang dibulat kan adalah 25.315 menjadi 30.000,

SELECT ROUND(125.315, 2, 1);
-- Hasil: 125.310 
-- Angka yang dibulat kan adalah 15 menjadi 10, dipotong menjadi 10 karena operator bernilai 1

```

### Detail Teknis

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server 2008 (diatas)                   | :heavy_check_mark: |
| Azure SQL Database                        | :heavy_check_mark: |
| . .         