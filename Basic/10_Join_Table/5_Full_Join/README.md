# FULL JOIN
![LEFT JOIN](https://www.w3schools.com/sql/img_fulljoin.gif)

`FULL JOIN` syntax yang digunakan untuk menampilkan suatu data atau record dengan menghubungkan dua table dalam satu kali perintah. Data yang ditampilkan pada `FULL JOIN` adalah semua data yang cocok antara tabel (table) kiri dan tabel (table) kanan.

## Syntax

```sql
SELECT column_name(s)
FROM table1
FULL OUTER JOIN table2
ON table1.column_name = table2.column_name;
```

## Contoh 

### Demo Database

Table: Customers                                                    
|  CustomerID  | CustomerName | ContactName | Address | City | PostalCode | Country |
| :--: | :-------: |:-------:| :-------: | :-------: |:-------:| :-------: |
|  1   | Alfreds Futterkiste  |  Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany
|  2   | Ana Trujillo Emparedados y helados |  Ana Trujillo   | Avda. de la Constitución 2222  | México D.F. | 05021 | Mexico
|  3   |   Antonio Moreno Taquería    |    Antonio Moreno    |    Mataderos 2312    | México D.F. | 05023 | Mexico

Table: Orders
| OrderID | CustomerID | EmployeeID | OrderDate | ShipperID |
| :------: | :-------: | :------: | :-------: | :------: |
|    10308    | 2      |     7    | 1996-09-18      |     3    |
|    10309    | 37      |     3    | 1996-09-19      |     1    |
|    10310    | 77      |     8    | 1996-09-20     |     2    |

### Contoh Syntax

```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
FULL OUTER JOIN Orders ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```

Karena diberikan syntax `FULL OUTER JOIN` untuk menggabungkan kedua table maka data yang diambil adalah semua data *CustomerName* dari tabel *Customers* serta data *OrderID* dari tabel *Orders*. 

Jika pada tabel kiri (*Customers*) dengan data *CustomerID* memiliki kesamaan pada *CustomerID* pada tabel kanan (*Orders*) maka data akan terisi jika tidak akan diisi **Null**. 

Berikut hasil dari Query SQL diatas:

### Hasil

| CustomerName | OrderID |
| :-------: | :-------: |
|  **Null**  | Math      | 
|  **Null**   | Math      |
|   Alfreds Futterkiste    | **Null**   | 
|   Ana Trujillo Emparedados y helados    | 10308   | 
|   Antonio Moreno Taquería    | **Null**   |


Terlihat dari hasil diatas bahwa yang *Ana Trujillo Emparedados y helados* yang memiliki hubungan antara kedua tabel tersebut, karena memiliki *CustomerID* 2 pada tabel *Orders*

### Catatan
- ```FULL OUTER JOIN``` dan ```FULL JOIN``` adalah sebuah fungsi yang sama.
