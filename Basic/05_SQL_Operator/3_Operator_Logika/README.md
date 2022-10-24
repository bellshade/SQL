# Operator Logika

Merupakan Operator yang digunakan untuk melakukan **mendapat** atau **membandingkan** antara 2 nilai logika benar (TRUE) dan salah (FALSE).

## Perintah Operator Logika

| Operator     | Deskripsi |
|---------|----------------------------------------------------------------|
| ALL     | TRUE jika semua data dari tabel utama berada di hasil subquery |
| AND     | TRUE jika 2 kondisi bernilai benar                             |
| ANY     | TRUE jika ada data dari tabel utama berada di hasil subquery   |
| BETWEEN | TRUE jika data berada di antara nilai perbandingan             |
| EXISTS  | TRUE jika hasil subquery mengembalikan 1 atau lebih data       |
| IN      | TRUE jika ada data yang serupa dengan nilai kondisi            |
| LIKE    | TRUE jika ada data yang serupa dengan nilai kondisi regex      |
| NOT     | Kebalikan dari nilai yang sekarang                             |
| OR      | TRUE jika salah satu kondisi bernilai benar                    |
| SOME    | TRUE jika ada data dari tabel utama berada di hasil subquery   |

## Contoh query

### ALL
Menampilkan data tabel Products, jika semua nilai dikolom ProductID ada di kolom ProductID tabel OrderDetails
```sql
SELECT ProductName 
FROM Products
WHERE ProductID = ALL (SELECT ProductID FROM OrderDetails WHERE Quantity = 10);
```

### AND
Menampilkan data tabel Customers, jika nilai dikolom City adalah London **DAN** Country adalak UK
```sql
SELECT * FROM Customers
WHERE City = "London" AND Country = "UK";
```

### ANY
Menampilkan data tabel Products, jika ada (minimal 1 data) nilai dikolom ProductID berada di kolom ProductID tabel OrderDetails
```sql
SELECT ProductName 
FROM Products
WHERE ProductID = ANY (SELECT ProductID FROM OrderDetails WHERE Quantity = 10);
```

### BETWEEN
Menampilkan data tabel Products, jika nilai di kolom Price berada diantara 50 dan 60
```sql
SELECT * FROM Products
WHERE Price BETWEEN 50 AND 60;
```

### EXISTS
Menampilkan data tabel Suppliers, jika nilai dikolom supplierID tabel Suppliers berada di kolom SupplierID tabel Products
```sql
SELECT SupplierName
FROM Suppliers
WHERE EXISTS (SELECT ProductName FROM Products WHERE Products.SupplierID = Suppliers.supplierID AND Price < 20);
```

### IN
Menampilkan data tabel Customers, jika nilai dikolom City adalah London atau Paris
```sql
SELECT * FROM Customers
WHERE City IN ('Paris','London');
```

### LIKE
Menampilkan data tabel Customers, jika nilai dikolom City berawalkan s

Penggunaan LIKE, dapat digabungkan dengan [Regex](https://dataschool.com/how-to-teach-people-sql/how-regex-works-in-sql/) untuk mencari data yang kita inginkan
```sql
SELECT * FROM Customers
WHERE City LIKE 's%';
```

### NOT
Menampilkan data tabel Customers, jika nilai dikolom City **bukan** London atau Paris
```sql
SELECT * FROM Customers
WHERE City NOT IN ('Paris','London');
```

### OR
Menampilkan data tabel Customers, jika nilai dikolom City adalah London **ATAU** Country adalak UK
```sql
SELECT * FROM Customers
WHERE City = "London" OR Country = "UK";
```

### SOME
Menampilkan data tabel Products, jika ada (minimal 1 data) nilai dikolom ProductID berada di kolom ProductID tabel OrderDetails
```sql
SELECT ProductName 
FROM Products
WHERE ProductID = SOME (SELECT ProductID FROM OrderDetails WHERE Quantity = 10);
```