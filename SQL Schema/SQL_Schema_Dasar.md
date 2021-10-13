# Schema dasar

Didalam sebuah **SQL Database** terdapat banyak **Schema** (**Skema**) yang bertujuan untuk memisahkan perngguan aplikasi yang berbeda dan pembagian hak akses.

Dalam sebuah **Schema** berisi beberapa objek seperti _Table_, _View_, _Store Procedure_ , _Function_ dan objek lainnya.

## Database Query

### Menampilkan Skema

```sql
SHOW DATABASES;
```

Setelah di eksekusi, akan muncul nama-nama **Schema** yang ada didalam database

![SHOW DATABASE](https://i.ibb.co/qxjNQXG/show-databases-mysql.png)

### Memilih Skema

Secara bawaan saat pertama kali mengakses **database**, **schema** yang terpilih adalah `master`, sehingga untuk mengakses **schema** lain kita gunakan query `USE`.

contoh nama **schema** adalah `bellshade_db`.

```sql
USE bellshade_db;
```

Query `USE` ini digunakan untuk mengubah _Schema_ yang ingin di akses di _database management tools_ seperti *SQL SERVER *atau* mysql workbench*,

### Membuat Skema

Untuk membuat **Schema** baru, nama **Schema** tidak boleh sama dengan **Schema** yang sudah ada.

contoh nama **schema** yang akan dibuat adalah `bellshade_test`.

```sql
CREATE DATABASE `bellshade_test`;
```

### Menghapus Skema

Untuk menghapus **Schema**, perhatikan bahwa yang akan terhapus adalah _Table_, _record_, _View_, _Store Procedure_ , _Function_ dan objek lainnya.

contoh nama **schema** yang akan dihapus adalah `bellshade_test` .

```sql
DROP DATABASE `bellshade_test`;
```

### Compatibility Query

| Relational Database Management | test syntax        |
| ------------------------------ | ------------------ |
| SQL Server                     | :heavy_check_mark: |
| MariaDB                        | :heavy_check_mark: |
