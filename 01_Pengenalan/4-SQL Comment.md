# SQL Comment
Comment / Komentar digunakan untuk menjelaskan dari query yang kita buat ataupun digunakan untuk mencegah suatu query berjalan

## Single Line Comment
Single line comment pada SQL dimulai dengan ```--```
Contoh dari penerapan single line comment adalah 
```sql
-- Memilih seluruh data dari kolom siswa
SELECT * FROM siswa
``` 
Penerapan SQL Comment diatas digunakan untuk memberikan keterangan terhadap query yang kita buat<br>
Sementara untuk melakukan pencegahan atas suatu query
```sql
SELECT * FROM siswa --WHERE jk == 'Pria';
``` 

## Multi Line Comment
Multi line comment pada SQL dimulai dengan ```/*``` dan di akhiri ```*/``` 
Contoh penerapannya adalah<br>
```SQL
/* Menampilkan data siswa
Dengan gender Perempuan*/
SELECT * FROM siswa WHERE jk == 'Perempuan';
```
