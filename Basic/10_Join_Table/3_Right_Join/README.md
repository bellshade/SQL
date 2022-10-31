# RIGHT JOIN
![LEFT JOIN](https://www.w3schools.com/sql/img_rightjoin.gif)

`RIGHT JOIN` syntax yang digunakan untuk menampilkan suatu data atau record dengan menghubungkan dua table atau lebih dalam satu kali perintah. Data yang ditampilkan pada `RIGHT JOIN` adalah semua data disebelah kanan tabel (table2) serta semua data dari tabel kiri (table1) yang memiliki kesamaan dengan tabel kanan (table2).

## Syntax

```sql
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
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
RIGHT JOIN class 
ON student.Class_Id = class.Class_ID
```

Karena diberikan syntax `RIGHT JOIN` untuk menggabungkan kedua table maka data yang diambil adalah semua data *Classname* dari tabel *class* serta data dari tabel *student* yang *class.Class_ID* nya sama dengan *student.Class_Id*. 

Jika pada tabel kiri (*student*) tidak memiliki kesamaan pada *class_id* pada tabel kanan (*class*) maka data yang ditampil adalah **Null**. 

Jika pada tabel kiri (*student*) memiliki kesamaan pada *class_id* pada tabel kanan (*class*) lebih dari 1 data, maka data **ditampilkan semua**. 

Berikut hasil dari Query SQL diatas:

### Hasil

| FirstName | ClassName |
| :-------: | :-------: |
|  Adellyn  | Math      | 
|  Lalisa   | Math      |
|   Jack    | Physics   | 
|   NULL    | English   |
