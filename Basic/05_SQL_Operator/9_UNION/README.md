# UNION
 
 ![Union_illustration-SQL_Union](https://user-images.githubusercontent.com/92574134/166089696-1b6dcd87-6b3e-468e-92dc-f939e63cad77.PNG)
 
### Operator **UNION** adalah operator untuk menggabungkan data dari dua atau lebih hasil perintah SELECT menjadi satu set data yang berbeda.
 
Hal yang harus diperhatikan ketika menggunakan UNION :
- Tipe data yang digunakan harus mirip (string, waktu, numerik, dll)
- Jumlah kolom yang dipilih oleh setiap perintah SELECT harus sama

Syntax UNION :
```sql
SELECT kolom_1, kolom_2, ...
FROM table_1
UNION
SELECT kolom_1, kolom_2, ...
FROM table_2
```

Contoh :
Membuat DATABASE kantor dengan 3 table:  
#### Table dept_pemasaran  
![Screenshot (145)](https://user-images.githubusercontent.com/92574134/166960507-c8367c8a-0e4e-47a3-87b3-f1873a20a1e0.png)  
#### Table dept_it  
![Screenshot (146)](https://user-images.githubusercontent.com/92574134/166964880-7d1e4bdb-3ed1-4bf8-8789-447867faeb16.png)  
#### Table dept_hrd  
![Screenshot (147)](https://user-images.githubusercontent.com/92574134/166967982-e82106dd-2e90-4a94-9af7-6acc337f228e.png)  

#### 1. Contoh dengan menggunakan 1 kolom dari masing masing 2 table
syntax :
```sql
SELECT Nama 
FROM dept_it
UNION
SELECT Nama 
FROM dept_pemasaran
```

Hasil :  
![Screenshot (148)](https://user-images.githubusercontent.com/92574134/166969622-dc20f2d0-a2e7-4c86-8b94-355c086fb890.png)
  
#### 2. Contoh menggunakan 2 kolom dari masing masing 2 table  
Syntax :  
```sql
SELECT Nama, Jabatan
FROM dept_it
UNION
SELECT Nama, Jabatan
FROM dept_pemasaran
```
Hasil :  
![Screenshot (149)](https://user-images.githubusercontent.com/92574134/166970889-83f6411b-65b3-4061-afc1-f121c64d08fa.png)  

#### 3. Contoh menggunakan 1 kolom dari masing masing 3 table  
Syntax :  
```sql
SELECT Nama
FROM dept_pemasaran
UNION 
SELECT Nama
FROM dept_hrd
UNION
SELECT Nama
FROM dept_it
```
Hasil :  
![Screenshot 2022-05-06 at 14-04-17 localhost _ 127 0 0 1 _ kantor phpMyAdmin 5 1 1](https://user-images.githubusercontent.com/92574134/167076093-d1fadbe8-fcac-43c4-bd5c-6e5e6629d3e0.png)  

[<< Materi sebelumnya](https://github.com/bellshade/SQL/tree/main/Basic/05_SQL_Operator/9_UNION)
