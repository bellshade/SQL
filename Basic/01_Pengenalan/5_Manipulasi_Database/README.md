#   Manipulasi Database

-`CREATE DATABASE`, digunakan untuk membuat database dengan format sebagai berikut:

```SQL
CREATE DATABASE [IF NOT EXISTS] nama database;
```
IF NOT EXISTS digunakan untuk memastikan database yang dibuat belum ada, namun tidak wajib dituliskan.

-`SHOW DATABASES`, digunakan untuk menampilkan daftar database yang telah dibuat.
-`USE`, digunakan untuk membuka database sehingga dapat memanipulasi tabel yang ada di dalamnya. Contoh:
```SQL
USE nama database;
```
-`DROP DATABASE`, digunakan untuk menghapus database dengan format sebagai berikut:
```SQL
DROP DATABASE [IF EXISTS] nama database;
```