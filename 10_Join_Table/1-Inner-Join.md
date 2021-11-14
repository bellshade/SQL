# INNER JOIN
![INNER JOIN](https://user-images.githubusercontent.com/93637835/140651112-d09d9473-c725-4e9c-9f8b-c122aa13a0b5.png)

`INNER JOIN` adalah syntax yang digunakan untuk menampilkan suatu data atau record dengan menghubungkan dua table atau lebih dalam satu kali perintah. Data yang ditampilkan pada `INNER JOIN` adalah data yang memiliki pasangan atau kesamaan pada semua table yang dihubungkan.

## Syntax

```sql
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```

## Contoh 

### Demo Database
Table: Student                                                    
|  ID  | FirstName | LastName | Class_Id |
| :--: | :-------: |:--------:| :------: |
|  01  | Franklin  |  Josh    |    00    |
|  02  | Adellyn   |  Brown   |    31    |
|  03  |   Jack    |    Ma    |    32    |
|  04  | Lalisa    |  Jeine   |    31    |

Table: Class
| Class_ID | ClassName |
| :------: | :-------: |
|    31    | Math      | 
|    32    | Physics   | 
|    33    | English   |
 

### Contoh Syntax

```sql
SELECT FirstName, ClassName
FROM Student INNER JOIN Class
ON Student.ClassID = Class.ID
```

Karena diberikan syntax `INNER JOIN` untuk menggabungkan kedua table maka data yang diambil hanyalah data yang memiliki pasangan pada masing-masing table. Sementara itu, data yang tidak memiliki pasangan seperti FirstName Franklin pada tabel Student dan ClassName English pada tabel Class tidak diambil karena tidak memiliki pasangan sehingga table yang dapat ditampilkan adalah sebagai berikut:

### Hasil

| FirstName | ClassName |
| :-------: | :-------: |
|  Adellyn  | Math      | 
|    Jack   | Physics   | 
|  Lalisa   | Math      |

## Referensi
https://www.w3schools.com/sql/sql_join_inner.asp
