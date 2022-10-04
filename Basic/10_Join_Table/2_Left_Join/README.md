# LEFT JOIN
![LEFT JOIN](https://www.w3schools.com/sql/img_leftjoin.gif)

`LEFT JOIN` syntax yang digunakan untuk menampilkan suatu data atau record dengan menghubungkan dua table atau lebih dalam satu kali perintah. Data yang ditampilkan pada `LEFT JOIN` adalah semua data disebelah kiri tabel (table1) serta semua data dari tabel kanan (table2) yang memiliki kesamaan dengan tabel kiri (table1).

## Syntax

```sql
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```

## Contoh 

### Demo Database

Table: student                                                    
|  ID  | FirstName | LastName | Class_Id |
| :--: | :-------: |:--------:| :------: |
|  1   | Franklin  |  Josh    |     0    |
|  2   | Adellyn   |  Brown   |    31    |
|  3   |   Jack    |    Ma    |    32    |
|  4   | Lalisa    |  Jeine   |    31    |

Table: class
| Class_ID | ClassName |
| :------: | :-------: |
|    31    | Math      | 
|    32    | Physics   | 
|    33    | English   |

### Contoh Syntax

```sql
SELECT FirstName, ClassName 
FROM student 
LEFT JOIN class 
ON student.Class_Id = class.Class_ID
```

Karena diberikan syntax `LEFT JOIN` untuk menggabungkan kedua table maka data yang diambil adalah semua data FirstName dari tabel student serta data dari tabel class yang class.Class_ID nya sama dengan student.Class_Id. Jika pada tabel kanan (class) tidak memiliki kesamaan pada class_id pada tabel 1 maka data yang ditampil adalah Null. Berikut hasil dari Query SQL diatas:

### Hasil

| FirstName | ClassName |
| :-------: | :-------: |
|  Franklin | _NULL_    |
|  Adellyn  | Math      | 
|   Jack    | Physics   | 
|  Lalisa   | Math      |
