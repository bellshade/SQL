# SQL Having

**Having** ditambahkan ke `SQL` Karena `WHERE` menempatkan kondisi pada `column` yang dipilih, sedangkan `HAVING` menempatkan kondisi pada gorup yang dibuat oleh `GROUP BY`  

### Having Syntax:
kode berikut menunjukan posisi `HAVING` pada query
```sql
SELECT expression_1, expression_2, ... expression_n,
       aggregate_function (aggregate_expression)
  FROM tables 
 WHERE condition 
GROUP BY expression_1, expression_2, ... expression_n
HAVING condition;
```

### Parameter atau Argumen
**_expression_1, expression_2, ... expression_n_**  
_expression_ yang tidak dienkapsulasi dalam fungsi agregate dan harus disertakan dalam  `GROUP BY` di dekat akhir pernyataan SQL.  

**_Aggregate_function_**
Ini adalah fungsi agregat seperti `SUM`, `COUNT`, `MIN`, `MAX`, atau `AVG`  

**_Aggregate_expression_**  
Ini adalah `column` atau ekspresi yang akan digunakan oleh fungsi agregat.

**_Tables_**  
Tabel yang igin anda gunakan, setidaknya harus ada satu tabel yang tercantum.

**_Where_**  
Opsional, Ini adalah kondisi yang akan dipilih. 

**_Having_**  
Ini adalah ketentuan yang hanya diterapkan pada hasil gabungan untuk membatasi baris grup yang dikembalikan, hanya group yang konsidinya bernilai `TRUE` yang akan di tampilkan pada hasil.

### Contoh:

```sql
SELECT A.customer_id, SUM(A.amount) total_amount
  FROM payment A
GROUP BY A.customer_id;
```
Table payment:

|     | customer_id | total_amount |
|-----|-------------|--------------|
| 1   | 184         | 80.8         |
| 2   | 87          | 137.72       |
| 3   | 477         | 106.79       |
| 4   | 273         | 130.72       |
| 5   | 550         | 151.69       |
| 6   | 51          | 123.7        |
| 7   | 394         | 77.8         |
| 8   | 272         | 65.87        |
| 9   | 70          | 75.83        |
| 10  | 190         | 102.75       |
| ..  | ...         | ...          |

#### Contoh Penggunaan `SUM` function
pernyataan berikut menambahkan `HAVING` untuk memilih satu `customer` yang telah berbelanja lebih dari `200`
```sql
SELECT A.customer_id, SUM(A.amount) total_amount
  FROM payment A
GROUP BY A.customer_id
HAVING SUM(A.amount) > 200;
```
**Result:**

|     | customer_id | total_amount |
|-----|-------------|--------------|
| 1   | 526         | 208.58       |
| 2   | 148         | 211.55       |

#### Contoh Penggunaan `COUNT` function
pernyataan berikut menambahkan `HAVING` untuk memilih satu `customer` yang melakukan pembelian lebih dari `30`
```sql
SELECT A.customer_id, COUNT(A.customer_id)
  FROM payment A
GROUP BY A.customer_id
having count(A.customer_id) > 30;
```
**Result:**

|     | customer_id | count |
|-----|-------------|-------|
| 1   | 550         | 31    |
| 2   | 406         | 31    |
| 3   | 176         | 32    |

#### Contoh Penggunaan `MIN` function
pernyataan brikut menambahkan `HAVING` untuk memilih satu `customer` yang melakukan pembelian dengan nilai `MIN` `amount` lebih dari `2`
```sql
SELECT A.customer_id, MIN(A.amount)
  FROM payment A
GROUP BY customer_id
having MIN(A.amount) > 2;
```
**Result:**

|     | customer_id | min  |
|-----|-------------|------|
| 1   | 363         | 2.99 |
| 2   | 59          | 2.99 |

#### Contoh Penggunaan `MAX` function
pernyataan brikut menambahkan `HAVING` untuk memilih satu `customer` yang melakukan pembelian dengan nilai `MAX` `amount` lebih dari `10`
```sql
SELECT A.customer_id, MAX(A.amount)
  FROM payment A
GROUP BY customer_id
having MAX(A.amount) > 10;
```
